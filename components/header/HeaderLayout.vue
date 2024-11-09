<template>
  <header class="header">
    <div class="container">
      <div class="header__wrap">
        <img class="header__logo" src="/img/logo.svg" alt="logo">
        <nav class="header__nav">
          <ul class="header__list list-reset">
            <li class="header__item"><NuxtLink class="header__link" to="/">Главная</NuxtLink></li>
            <li class="header__item"><a class="header__link" @click="scroll1">О нас</a></li>
            <li class="header__item"><a class="header__link" @click="scroll2">Контакты</a></li>
            <li class="header__item"><a class="header__link" @click="scroll3">Проекты</a></li>
          </ul>
        </nav>
        <button class="header__btn btn-reset" @click="OpenPopup">Контакты</button>
        <CommonPopUp style="position: absolute;" v-if="isOpen" @close-form="close"/>
      </div>
    </div>
  </header>
</template>

<script lang="ts" setup>
import gsap from 'gsap'
import { ScrollTrigger } from 'gsap/ScrollTrigger'
import { ScrollToPlugin } from 'gsap/ScrollToPlugin'

gsap.registerPlugin(ScrollToPlugin)
gsap.registerPlugin(ScrollTrigger)

const isOpen = ref(false)
const close = () => {
  isOpen.value = false
}

const OpenPopup = () => {
  isOpen.value = true
}

const scroll1 = () => {
  const scrollSection1 = document.getElementById('about')
  if (scrollSection1) {
    gsap.to(window, {
      duration: 1.5,
      scrollTo: { y: scrollSection1, offsetY: 20 },
      ease: 'power2.inOut'
    })
  }
}
const scroll2 = () => {
  const scrollSection2 = document.getElementById('contacts')
  if (scrollSection2) {
    gsap.to(window, {
      duration: 1.5,
      scrollTo: { y: scrollSection2, offsetY: 20 },
      ease: 'power2.inOut'
    })
  }
}
const scroll3 = () => {
  const scrollSection3 = document.getElementById('projects')
  if (scrollSection3) {
    gsap.to(window, {
      duration: 1.5,
      scrollTo: { y: scrollSection3, offsetY: 20 },
      ease: 'power2.inOut'
    })
  }
}
</script>

<style lang="scss" scoped>
.header {
  padding-bottom: 80px;
  &__wrap {
    padding: 10px 0px;
    display: flex;
    justify-content: space-between;
    align-items: center;
  }
  &__list {
    display: flex;
    gap: 70px;
  }
  &__link {
    position: relative;
		color: #000;
		font-family: 'Akrobat';
		font-size: 25px;
		font-style: normal;
		font-weight: 400;
    text-decoration: none;
    cursor: pointer;
    transition: color 0.3s ease-in-out;
    &::after {
      content: '';
      position: absolute;
      bottom: -5px;
      left: 0;
      width: 100%;
      height: 2px;
      background-color: #029444;
      transform: scaleX(0);
      transition: transform 0.3s ease-in-out;
    }
    &:hover::after {
    transform: scaleX(1);
    }
    &:hover {
      color: #029444;
    }
  }
  &__logo {
    color: #000;
		font-family: 'Akrobat';
		font-size: 25px;
		font-style: normal;
		font-weight: 400;
  }
  &__btn {
  background: #000;
  border-radius:30px;
  padding: 10px 45px;
    color: #ffffff;
		font-family: 'Akrobat';
		font-size: 18px;
		font-style: normal;
		font-weight: 400;
    transition: background 0.3s ease-in-out, color 0.3s ease-in-out;
    &:hover {
      background: #029444;
      color: #ffffff;
    }
  } 
&__logo {
  width: 200px;
  height: 200px;
}

}
</style>