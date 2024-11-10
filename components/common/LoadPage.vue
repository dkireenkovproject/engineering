<template>
  <div class="loading-spinner">
    <div class="loading-spinner__progress">
      <img class="img" src="/img/logo-load.jpg" alt="Loading..." />
      <span class="loading-spinner__progress-text">Поставляем и налаживаем инженерное оборудование... {{ progress }}%</span>
  </div>
  </div>
</template>

<script lang="ts" setup>
import { ref, onMounted } from 'vue';
import { gsap } from 'gsap';

const progress = ref(0)

onMounted(() => {
  gsap.to('.img', {
    rotation: 360,
    repeat: -1, 
    duration: 2,
    ease: 'linear',
  });
  gsap.to(progress, {
    value: 100,
    duration: 2, 
    ease: 'power1.inOut',
    onUpdate: () => {
      progress.value = Math.round(progress.value)
    },
  })
});
</script>

<style scoped lang="scss">
.loading-spinner {
  position: fixed;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  z-index: 9999; 
}
.img {
  margin-bottom: 40px;
  width: 100px;
  height: auto;
}

.loading-spinner__progress {
display: flex;
flex-direction: column;
align-items: center;
}
.loading-spinner__progress-text {
  display: block;
  text-align: center;
  color: #000000;
    font-family: 'Akrobat';
    font-size: 25px;
    font-style: normal;
    font-weight: 700;
    @media screen and (max-width: 480px) {
      font-size: 18px;
    }
    @media screen and (max-width: 380px) {
      font-size: 14px;
    }
}
</style>
