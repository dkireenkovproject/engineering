<template>
  <section class="partners">
      <div class="partners__wrap">
    <h3 class="partners__title">Наши партнеры:</h3>
    <Vue3Marquee>
      <img class="partners__img" src="/img/partners-1.png" alt="partners-1" />
      <img class="partners__img" src="/img/partners-2.png" alt="partners-2" />
      <img class="partners__img" src="/img/partners-3.png" alt="partners-3" />
      <img class="partners__img" src="/img/partners-4.png" alt="partners-4" />
      <img class="partners__img" src="/img/partners-5.png" alt="partners-5" />
      <img class="partners__img" src="/img/partners-6.png" alt="partners-6" />
      <img class="partners__img" src="/img/partners-7.png" alt="partners-7" />
      <img class="partners__img" src="/img/partners-8.png" alt="partners-8" />
      <img class="partners__img" src="/img/partners-9.png" alt="partners-9" />
      <img class="partners__img" src="/img/partners-10.png" alt="partners-10" />
      <img class="partners__img" src="/img/partners-11.png" alt="partners-11" />
      <img class="partners__img" src="/img/partners-12.png" alt="partners-12" />
      <img class="partners__img" src="/img/partners-13.png" alt="partners-13" />
    </Vue3Marquee>
  </div>
  </section>
</template>

<script lang="ts" setup>
import { Vue3Marquee } from 'vue3-marquee'

</script>

<style lang="scss" scoped>
.partners {
  padding-bottom: 50px;
   &__img {
    display: inline-block; 
    margin-right: 50px;
max-width: 250px;
    height: auto;
  }
  &__title {
    text-align: center;
    color: #000000;
		font-family: 'Akrobat';
		font-size: 35px;
		font-style: normal;
		font-weight: 400;
  }
  &__wrap {
    display: flex;
    align-items: center;
  }
}
</style>