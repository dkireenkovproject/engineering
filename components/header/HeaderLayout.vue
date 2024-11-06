<template>
  <header class="header">
    <div class="container">
      <div class="header__wrap">
        <span class="header__logo">B3 Development</span>
        <nav class="header__nav">
          <ul class="header__list list-reset">
            <li class="header__item"><NuxtLink class="header__link" to="/">Главная</NuxtLink></li>
            <li class="header__item"><NuxtLink class="header__link" to="/">О нас</NuxtLink></li>
            <li class="header__item"><NuxtLink class="header__link" to="/">Контакты</NuxtLink></li>
            <li class="header__item"><NuxtLink class="header__link" to="/">Проекты</NuxtLink></li>
          </ul>
        </nav>
        <button class="header__btn btn-reset">Контакты</button>
      </div>
    </div>
  </header>
</template>

<script lang="ts" setup>

</script>

<style lang="scss" scoped>
.header {
  padding-bottom: 80px;
  &__wrap {
    padding: 50px 0px;
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


}
</style>