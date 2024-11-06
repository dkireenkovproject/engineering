<template>
  <footer class="footer">
    <div class="container">
      <div class="footer__wrapper">
        <div class="footer__top">
          <h2 class="footer__title">Б3 Девелопмент</h2>
          <nav class="footer__nav">
            <!-- <h3 class="footer__subtitle">Навигация</h3> -->
            <ul class="footer__items list-reset">
              <li class="footer__item"><NuxtLink to="/" class="footer__link">О нас</NuxtLink></li>
              <li class="footer__item"><NuxtLink to="/" class="footer__link">Проекты</NuxtLink></li>
              <li class="footer__item"><NuxtLink to="/" class="footer__link">Контакты</NuxtLink></li>
            </ul>
          </nav>
  

          <nav class="footer__nav">
            <ul class="footer__items list-reset">
              <li class="footer__item"><span class="footer__text">Офис в Москве: </span><span href="tel:+74991107987" class="footer__link">ул. Примерная, дом 1, офис 101</span></li>
              <li class="footer__item"><span class="footer__text">Телефон: </span><a href="tel:+74991107987" class="footer__link">+7 (499) 110-7987</a></li>
            </ul>
          </nav>

      
        </div>
        <div class="footer__bottom">
          <span class="footer__dash"></span>
          <p class="footer__copyright">© 2024 Б3 Девелопмент. Все права защищены.</p>
        </div>
        <!-- <nav class="footer__nav">
          <ul class="footer__items list-reset">

            <li class="footer__item">
              <h2 class="footer__title">Б3 Девелопмент</h2>
              <p class="footer__copyright">© 2024 Б3 Девелопмент. Все права защищены.</p>
            </li>

            
            <li class="footer__item">
              <h3 class="footer__subtitle">Навигация</h3>
              <ul class="footer__subitems list-reset">
                <li class="footer__item"><NuxtLink to="/" class="footer__subitem">О нас</NuxtLink></li>
                <li class="footer__item"><NuxtLink to="/" class="footer__subitem">Контакты</NuxtLink></li>
                <li class="footer__item"><NuxtLink to="/" class="footer__subitem">Проекты</NuxtLink></li>
              </ul>
            </li>

            
            <li class="footer__item">
              <a class="footer__link" href="tel:+79999999999">+7 (999) 197 83 47</a>
              <a class="footer__link" href="tel:+79999999999">+7 (999) 197 83 47</a>
              <a class="footer__link" href="mailto:B3Development@gmail.com">B3Development@gmail.com</a>
            </li>
          </ul>
        </nav> -->
      </div>
    </div>
  </footer>
</template>

<script lang="ts" setup>

</script>

<style lang="scss" scoped>
.footer {
  padding: 70px 0;
  &__top {
    display: flex;
    align-items: center;
    justify-content: center;
    gap: 50px;
    margin-bottom: 50px;
  }
&__dash {
  margin-bottom: 30px;
  display: block;
  width: 100%;
  height: 1px;
  background: #000000;
}
&__copyright {
  text-align: center;
    color: #000000;
    font-family: 'Akrobat';
    font-size: 18px;
    font-style: normal;
    font-weight: 400;
  }
    &__title {
    color: #000000;
    font-family: 'Akrobat';
    font-size: 22px;
    font-style: normal;
    font-weight: 400;
  }
    &__items {
    display: flex;

gap: 25px;
  }
  &__link {
    color: #000000;
    font-family: 'Akrobat';
    font-size: 18px;
    font-style: normal;
    font-weight: 400;
  }
  &__nav {
    display: flex;
    flex-direction: column;
    justify-content: center;
  }
  &__subtitle {
    margin-bottom: 10px;
    display: block;
    color: #000000;
    font-family: 'Akrobat';
    font-size: 24px;
    font-style: normal;
    font-weight: 400;
  }
&__text {
  color: #000000;
    font-family: 'Akrobat';
    font-size: 18px;
    font-style: normal;
    font-weight: 400;
}
  // &__items {
  //   display: flex;
  //   justify-content: space-between;
  //   align-items: center;
  // }

  // &__item {
  //   display: flex;
  //   flex-direction: column;
  //   gap: 10px;
  // }

  // &__subtitle {
  //   display: block;
  //   color: #ffffff;
  //   font-family: 'Akrobat';
  //   font-size: 24px;
  //   font-style: normal;
  //   font-weight: 400;
  // }

  // &__title {
  //   text-align: center;
  //   color: #ffffff;
  //   font-family: 'Akrobat';
  //   font-size: 18px;
  //   font-style: normal;
  //   font-weight: 400;
  // }

  // &__copyright {
  //   text-align: center;
  //   color: #ffffff;
  //   font-family: 'Akrobat';
  //   font-size: 18px;
  //   font-style: normal;
  //   font-weight: 400;
  // }

  // &__link {
  //   text-align: center;
  //   color: #ffffff;
  //   font-family: 'Akrobat';
  //   font-size: 18px;
  //   font-style: normal;
  //   font-weight: 400;
  // }

  // &__subitem {
  //   text-align: center;
  //   color: #ffffff;
  //   font-family: 'Akrobat';
  //   font-size: 18px;
  //   font-style: normal;
  //   font-weight: 400;
  //   &:nth-last-child(1) {
  //     margin-bottom: 5px;
  //   }
  // }

}
</style>
