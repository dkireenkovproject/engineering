<template>
  <section id="projects" class="project">
    <div class="container">
      <div class="project__wrapper-content">
      <h2 class="project__title">Наши последние проекты</h2>
      <p class="project__description">Наше портфолио — это примеры проектов, выполненных с акцентом на качество, передовые технологии и индивидуальный подход к потребностям клиентов.</p>
    <ul class="project__list list-reset">
      <li class="project__item">
          <img class="project__img" src="/img/1.jpg" alt="project1">
          <p class="project__text">HILTON GARDEN INN GOLDEN GATE
          </p>
      </li>
      <li class="project__item">
        <img class="project__img" src="/img/2.jpg" alt="project2">
                  <p class="project__text">Культурно-развлекательный комплекс в городе Магас</p>

      </li>
      <li class="project__item">
        <img class="project__img" src="/img/3.jpg" alt="project3">
                  <p class="project__text">SQUIRE PATTON BOGGS
                  </p>

      </li>
      <li class="project__item">
        <img class="project__img" src="/img/4.jpg" alt="project4"> 
                <p class="project__text">Офис компании NAVIGATOR
                </p>
     </li>
      <li class="project__item">
        <img class="project__img" src="/img/5.jpg" alt="project5"> 
                <p class="project__text">Частные апартаменты в гостинице «МОСКВА» («FOUR SEASONS»)
                </p>
     </li>
      <li class="project__item">
        <img class="project__img" src="/img/6.jpg" alt="project6">  
                <p class="project__text">Проектирование кинозалов, поставка, монтаж, настройка оборудования
                </p>
    </li>
    </ul>
    </div>
    </div>
  </section>
</template>

<script lang="ts" setup>
import { onMounted } from 'vue'
import { gsap } from 'gsap'
import { ScrollTrigger } from 'gsap/ScrollTrigger'

gsap.registerPlugin(ScrollTrigger)

onMounted(() => {
  gsap.from('.project', {
    y: 300,                
    opacity: 0,          
    duration: 1.5,        
    ease: 'power4.out',    
    scrollTrigger: {
      trigger: '.project',  
      start: 'top 70%',      
    },
  })

 gsap.from('.project__item', {
    y: 0,               
    opacity: 0,           
    duration: 1.5,        
    stagger: 0.3,          
    ease: 'power4.out',   
    scrollTrigger: {
      trigger: '.project__list', 
      start: 'top 50%',           
    },
  })
  const images = document.querySelectorAll('.project__img')

  images.forEach(image => {
    image.addEventListener('mouseenter', () => {
      gsap.to(image, {
        scale: 1.05,
        duration: 0.3,
        ease: 'power2.out',
      })
    })

    image.addEventListener('mouseleave', () => {
      gsap.to(image, {
        scale: 1,
        duration: 0.3,
        ease: 'power2.out',
      })
    })
  })
})
</script>

<style lang="scss" scoped>
.project {
  padding-bottom: 150px; 
  @media screen and (max-width: 600px) {
    padding-bottom: 100px; 
  }
  &__title {
  margin-bottom: 50px;
    color: #000000;
    font-family: 'Akrobat';
    font-size: 35px;
    font-style: normal;
    font-weight: 700;
    @media screen and (max-width: 1482px) {
      margin-bottom: 30px;
    }
    @media screen and (max-width: 600px) {
      margin-bottom: 30px;
      font-size: 28px;
    }
}
&__description {
  margin-bottom: 35px;
  max-width: 700px;
  text-align: center;
    color: #000000;
    font-family: 'Akrobat';
    font-size: 20px;
    font-style: normal;
    font-weight: 400;
    @media screen and (max-width: 1482px) {
      font-size: 18px;
    }
    @media screen and (max-width: 600px) {
      font-size: 16px;
    }
}
&__wrapper-content {
      display: flex;
      flex-direction: column;
     align-items: center;
    }
    &__list {
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      gap: 30px;
      row-gap: 70px;
      @media screen and (max-width: 1300px) {
        grid-template-columns: repeat(2, 1fr);
    }
    @media screen and (max-width: 600px) {
      grid-template-columns: repeat(1, 1fr);
    }
    }
    &__img {
    width: 100%;
    height: 100%;
    object-fit: cover;
    margin-bottom: 20px;
  }
  &__text {
    display: block;
    margin-bottom: 20px;
    text-align: center ;
    color: #000000;
    font-family: 'Akrobat';
    font-size: 20px;
    font-style: normal;
    font-weight: 400;
    @media screen and (max-width: 1482px) {
      font-size: 18px;
    }
    @media screen and (max-width: 600px) {
      font-size: 16px;
    }
  }

}
</style>