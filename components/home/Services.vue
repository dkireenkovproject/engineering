<template>
  <section class="services">
    <div class="container">
      <h2 class="services__title">
        Наши услуги
      </h2>
      <ul class="services__items list-reset">
        <li class="services__item">
          <img class="services__img" alt="services-1" src="/img/pic-1.png">
          <h3 class="services__subtitile">Монтаж инженерных систем</h3>
          <p class="services__description">Наша команда экспертов обеспечивает надежную и точную установку современных инженерных систем, соответствующих потребностям вашего проекта.</p>
        </li>
        <li class="services__item">
          <img class="services__img" alt="services-1" src="/img/pic-2.png">
           <h3 class="services__subtitile">Монтаж системы отопления, вентиляции и кондиционирования воздуха</h3>
          <p class="services__description">Мы предоставляем первоклассные услуги по установке систем отопления, вентиляции и кондиционирования воздуха, обеспечивая оптимальный климат-контроль и энергоэффективность в вашем здании.</p>
        </li>
        <li class="services__item">
          <img class="services__img" alt="services-1" src="/img/pic-3.png">
           <h3 class="services__subtitile">Настройка электрической системы</h3>
          <p class="services__description">Наши опытные специалисты выполняют безопасный и эффективный монтаж электросистем, отвечающий вашим конкретным требованиям.</p>
        </li>
        <li class="services__item">
          <img class="services__img" alt="services-1" src="/img/pic-4.png">
           <h3 class="services__subtitile">Решения по очистке воды</h3>
          <p class="services__description">Мы предлагаем комплексные установки по очистке воды, обеспечивающие чистое и безопасное водоснабжение для промышленных целей.</p>
        </li>
      </ul>
    </div>
  </section>
</template>

<script lang="ts" setup>
import { onMounted } from 'vue'
import { gsap } from 'gsap'
import { ScrollTrigger } from 'gsap/ScrollTrigger'

gsap.registerPlugin(ScrollTrigger)

onMounted(() => {
  gsap.from('.services', {
    y: 300,               
    opacity: 0,         
    duration: 1.5,        
    ease: 'power4.out',   
    scrollTrigger: {
      trigger: '.services',  
      start: 'top 80%',      
    },
  })
})
</script>

<style lang="scss" scoped>
.services {
padding-bottom: 200px;
&__title {
  margin-bottom: 70px;
  text-align: center;
    color: #000000;
    font-family: 'Akrobat';
    font-size: 35px;
    font-style: normal;
    font-weight: 700;
}
&__img {
  width: 100%;
  max-width: 350px;
  height: auto;
  border-radius: 4px;
}
&__items {
  display: grid;
  gap: 50px;
  grid-template-columns: repeat(4, 1fr);
}
&__item {
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 23px;
}
&__description {
  max-width: 330px;
  text-align: center;
    color: #000000;
    font-family: 'Akrobat';
    font-size: 16px;
    font-style: normal;
    font-weight: 400;
}
&__subtitile {
  text-align: center;
    color: #000000;
    font-family: 'Akrobat';
    font-size: 18px;
    font-style: normal;
    font-weight: 600;
}
}
</style>