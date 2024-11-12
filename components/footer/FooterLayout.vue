<template>
  <footer id="contacts" class="footer">
    <div class="container">
      <div class="footer__wrapper">
        <div class="footer__top">
          <h2 class="footer__title">Б3 Девелопмент</h2>
          <nav class="footer__nav">
            <ul class="footer__items list-reset">
              <li class="footer__item"><NuxtLink to="/" class="footer__link">О нас</NuxtLink></li>
              <li class="footer__item"><NuxtLink to="/" class="footer__link">Проекты</NuxtLink></li>
              <li class="footer__item"><NuxtLink to="/" class="footer__link">Контакты</NuxtLink></li>
            </ul>
          </nav>
  

          <nav class="footer__nav">
            <ul class="footer__items footer__mobile list-reset">
              <li class="footer__item"><span class="footer__text">Адрес: </span><span href="tel:+74991107987" class="footer__link">143502, Московская Область, г.о. Истра, г Истра, ул Почтовая, зд. 4А</span></li>
              <li class="footer__item"><span class="footer__text">Телефон: </span><a href="tel:+74993412124" class="footer__link">+7 (499) 341-21-24</a></li>
            </ul>
          </nav>

      
        </div>
        <div class="footer__bottom">
          <span class="footer__dash"></span>
          <p class="footer__copyright">© 2024 Б3 Девелопмент. Все права защищены.</p>
        </div>
      </div>
    </div>
  </footer>
</template>

<script lang="ts" setup>

</script>

<style lang="scss" scoped>
.footer {
  padding: 70px 0;
  @media screen and (max-width: 1300px) {
    padding: 0 0 70px 0;
  }
  &__top {
    display: flex;
    align-items: center;
    justify-content: center;
    gap: 50px;
    margin-bottom: 50px;
    @media screen and (max-width: 1300px) {
   flex-wrap: wrap;
   row-gap: 20px;
  }
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
    @media screen and (max-width: 350px) {
      font-size: 17px;
  }
}
&__mobile {
  @media screen and (max-width: 600px) {
    flex-direction: column;
    align-items: center;
    gap: 20px;
  }
}
&__item {
  text-align: center;
}
}
</style>
