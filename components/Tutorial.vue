<template>
  <div class="d-flex justify-content-center" style="height: 100vh">
    <img src="~/assets/img/bcg.jpg" class="bcgja" alt="bcg">
    <img src="~/assets/img/gaaaay.gif" alt="flag" style="width: 700px;">
    <div>
      <div class="waviy d-flex" style="min-width: max-content; margin-bottom: 80px;">
        <span v-for="(letter, idx) in arrayText" class="d-block" :style="`--i:${idx + 1}; ${letter !== ' ' ? '' : 'width: 20px;'}`">{{letter}}</span>
      </div>
<!--      <img class="m-auto" src="~/assets/img/zojaGay.jpg" alt="zoja gay" style="width: 500px">-->
    </div>
    <img src="~/assets/img/gaaaay.gif" alt="flag" style="transform: scaleX(-1); width: 700px;">
  </div>
</template>

<script>
export default {
  name: 'NuxtTutorial',
  data(){
    return{
      text: 'PROUD TO BE GAY'
    }
  },
  computed:{
    arrayText(){
      return this.text.split('');
    }
  }
}
</script>
<style>
@import url('https://fonts.googleapis.com/css2?family=Alfa+Slab+One&display=swap');

.bcgja{
  position: absolute;
  top: 0;
  right: 0;
  left: 0;
  bottom: 0;
  z-index: -1;
  width: 100%;
  height: 100vh;
}

.waviy {
  position: relative;
  -webkit-box-reflect: below -20px linear-gradient(transparent, rgba(0,0,0,.2));
  font-size: 60px;

}
.waviy span {
  font-family: 'Alfa Slab One', cursive;
  position: relative;
  display: inline-block;
  background: linear-gradient(
    90deg,
    rgba(255, 0, 0, 1) 0%,
    rgba(255, 154, 0, 1) 10%,
    rgba(208, 222, 33, 1) 20%,
    rgba(79, 220, 74, 1) 30%,
    rgba(63, 218, 216, 1) 40%,
    rgba(47, 201, 226, 1) 50%,
    rgba(28, 127, 238, 1) 60%,
    rgba(95, 21, 242, 1) 70%,
    rgba(186, 12, 248, 1) 80%,
    rgba(251, 7, 217, 1) 90%,
    rgba(255, 0, 0, 1) 100%
  );
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  text-transform: uppercase;
  animation: waviy 1s infinite;
  animation-delay: calc(.1s * var(--i));

}
@keyframes waviy {
  0%,40%,100% {
    transform: translateY(0)
  }
  20% {
    transform: translateY(-20px)
  }
}
</style>
