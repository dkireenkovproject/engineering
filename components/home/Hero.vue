<template>
  <section id="about" class="hero">
    <div class="container">
      <div class="hero__content">
      <div class="hero__wrapper-1">
        <h1 class="hero__title hero__animation">
          О компании B3 Development
        </h1>
        <p class="hero__description hero__animation">Компания Б3 Девелопмент была основана в 2015 году группой единомышленников с целью внедрения и оптимизации взаимодействия проектирования и монтажа инженерных систем. Мы стремимся предложить строительной отрасли решения, которые повышают ее эффективность и устойчивость.</p>
        <p class="hero__description hero__animation">Мы всегда нацелены на то, чтобы превосходить ожидания клиентов, ставя качество и инновации на первый план.</p>
        <p class="hero__description hero__animation">На нашем счету уже десятки успешных проектов, выполненных командой опытных специалистов, которая гарантирует точность и высокий стандарт на каждом этапе работы. За годы работы компания завоевала доверие множества клиентов, став надежным партнером для многих.
        </p>
        <p class="hero__description hero__animation">Наши принципы — честность, инновации и сотрудничество. Эти ценности определяют наш подход к каждому проекту и лежат в основе нашей работы. Присоединяйтесь к нам в преобразовании строительной отрасли с помощью передовых инженерных решений.
        </p>

        <!-- <ul class="hero__list list-reset">
        <li class="hero__item">
          <span class="hero__number">{{ procent }}
            %</span>
          <p class="hero__text hero__animation">Мы стремимся превзойти ожидания клиентов благодаря нашему стремлению к совершенству и инновациям.</p>
        </li>
        <li class="hero__item">
          <span class="hero__number">
{{ projects }} проектов</span>
          <p class="hero__text hero__animation">Честность, инновации и сотрудничество - вот основные ценности, которыми мы руководствуемся в своей работе и взаимоотношениях.</p>
        </li>
        <li class="hero__item">
          <span class="hero__number">{{ team }} членов команды</span>
          <p class="hero__text hero__animation">Благодаря сплоченной команде мы гарантируем, что каждый проект будет выполнен с точностью и тщательностью.</p>
        </li>
        <li class="hero__item">
          <span class="hero__number"> {{ clients }} обслуженных клиентов</span>
          <p class="hero__text hero__animation">Присоединяйтесь к нам в нашем стремлении изменить строительный ландшафт с помощью передовых инженерных решений.</p>
        </li>
      </ul> -->
      </div>
      <div class="hero__wrapper-2">
        <div class="hero__wrapper-3">
        <img class="hero__img" src="/img/hero.png" alt="hero-img">
      </div>
      </div>
    </div>
    </div>
  </section>
</template>

<script lang="ts" setup>
import { ref, onMounted } from 'vue'
import { gsap } from 'gsap';
import { ScrollTrigger } from 'gsap/ScrollTrigger'

gsap.registerPlugin(ScrollTrigger)

const procent = ref(0)
const projects = ref(0)
const team = ref(0)
const clients = ref(0)
const animation = ref(null)

onMounted(() => {
  gsap.to(procent, {
    value: 100,
    duration: 2, 
    ease: 'power1.inOut',
    onUpdate: () => {
      procent.value = Math.round(procent.value)
    },
  })
  gsap.to(projects, {
    value: 100,
    duration: 2, 
    ease: 'power1.inOut',
    onUpdate: () => {
      projects.value = Math.round(projects.value)
    },
  })
  gsap.to(team, {
    value: 50,
    duration: 2, 
    ease: 'power1.inOut',
    onUpdate: () => {
      team.value = Math.round(team.value)
    },
  })
  gsap.to(clients, {
    value: 1000,
    duration: 2, 
    ease: 'power1.inOut',
    onUpdate: () => {
      clients.value = Math.round(clients.value)
    },
  })
  const animatedElements = gsap.utils.toArray('.hero__animation')
  gsap.from(animatedElements, {
    y: 100,
    opacity: 0,
    duration: 1.5,
    ease: 'power2.out',
  });
});
</script>

<style lang="scss" scoped>
.hero {
  padding-bottom: 120px;
  @media screen and (max-width: 1300px) {
    padding-bottom: 150px;
  }
  @media screen and (max-width: 600px) {
    padding-bottom: 100px;
    }
&__content {
  display: flex;
  gap: 50px;
  align-items: center;
  justify-content: center;
  @media screen and (max-width: 1300px) {
  flex-direction: column;
  justify-content: space-between;
    }
}
&__list {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  gap: 20px;
  @media screen and (max-width: 879px) {
    grid-template-columns: repeat(1, 1fr);
  }
}
&__wrapper-1 {
  display: flex;
  flex-direction: column;
  width: 50%;
  @media screen and (max-width: 1300px) {
    width: 100%;
    }
}
&__title {
  margin-bottom: 50px;
  color: #000;
		font-family: 'Akrobat';
		font-size: 45px;
		font-style: normal;
		font-weight: 700;
    @media screen and (max-width: 1300px) {
      margin-bottom: 40px;
      font-size: 35px;
    }
    @media screen and (max-width: 600px) {
      margin-bottom: 30px;
      font-size: 28px;
    }
}
&__description {
  margin-bottom: 50px;
  color: #000;
		font-family: 'Akrobat';
		font-size: 20px;
		font-style: normal;
		font-weight: 400;
    @media screen and (max-width: 1300px) {
      margin-bottom: 40px;
      font-size: 18px;
    }
    @media screen and (max-width: 879px) {
      margin-bottom: 30px;
      &:last-child {
        margin-bottom: 0;
      }
    }
}
&__number {
  display: block;
  margin-bottom: 20px;
  color: #000;
		font-family: 'Akrobat';
		font-size: 30px;
		font-style: normal;
		font-weight: 700;
    @media screen and (max-width: 1300px) {
      font-size: 25px;
    }
    @media screen and (max-width: 879px) {
      margin-bottom: 10px;
    }
}
&__text {
  color: #000;
		font-family: 'Akrobat';
		font-size: 16px;
		font-style: normal;
		font-weight: 400;
}
&__wrapper-3 {
  width: 100%;
  @media screen and (max-width: 400px) {
    display: none;
  }
}
&__wrapper-2 {
  @media screen and (max-width: 400px) {
    display: none;
  }
}
&__img {
  object-fit: cover;}
}
</style>