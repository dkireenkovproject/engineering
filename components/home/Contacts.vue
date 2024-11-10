<template>
  <section id="contacts" class="contacts">
    <div class="container">
      <h2 class="contacts__title">Контакты</h2>

      <div class="contacts__wrapper">
        <div class="contacts__card">
          <h3 class="contacts__name">Алексей Баранов (Генеральный директор)
          </h3>
          <div class="contacts__ph-mail">
            <div class="contacts__style-wrap"><img class="contacts__style-img" src="/img/mail.png" alt="mail"><a class="contacts__style-link" href="mailto:alebar@b3-d.ru">alebar@b3-d.ru
            </a></div>
            <div class="contacts__style-wrap"><img class="contacts__style-img" src="/img/telephone.png" alt="telephone"><a class="contacts__style-link" href="tel:+79253916402">+7 (925) 391-6402
            </a></div>
            </div>
        </div>

        <div class="contacts__card">
          <h3 class="contacts__name">Подольский Александр (Руководитель проектов)
          </h3>
          <div class="contacts__ph-mail">
            <div class="contacts__style-wrap"><img class="contacts__style-img" src="/img/mail.png" alt="mail"><a class="contacts__style-link" href="mailto:alepod@b3-d.ru">alepod@b3-d.ru
            </a></div>
            <div class="contacts__style-wrap"><img class="contacts__style-img" src="/img/telephone.png" alt="telephone"><a class="contacts__style-link" href="tel:+79265033953">+7 (926) 503-3953
            </a></div>
            </div>
        </div>

        <div class="contacts__card">
          <h3 class="contacts__name">Маргарита Тарасова (Директор по развитию)</h3>
          <div class="contacts__ph-mail">
            <div class="contacts__style-wrap"><img class="contacts__style-img" src="/img/mail.png" alt="mail"><a class="contacts__style-link" href="mailto:martar@b3-d.ru">martar@b3-d.ru
            </a></div>
            <div class="contacts__style-wrap"><img class="contacts__style-img" src="/img/telephone.png" alt="telephone"><a class="contacts__style-link" href="tel:+79255546959">+7(925) 554-6959
            </a></div>
            </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script lang="ts" setup>

</script>

<style lang="scss" scoped>
.contacts {
  padding-bottom: 100px;
  @media screen and (max-width: 1300px) {
    padding-bottom: 150px;
    }
    @media screen and (max-width: 600px) {
      padding-bottom: 100px;
    }
  &__title {
    margin-bottom: 40px;
    text-align: center;
    color: #000000;
    font-family: 'Akrobat';
    font-size: 35px;
    font-style: normal;
    font-weight: 700;
    @media screen and (max-width: 600px) {
      margin-bottom: 30px;
      font-size: 28px;
    }
  }
  &__ph-mail {
    display: flex;
    flex-direction: column;
    gap: 5px;
    @media screen and (max-width: 600px) {
      align-items: center;
    }
  }
&__style-wrap {
  display: flex;
  align-items: center;
  gap: 5px;
}
&__style-img {
  width: 20px;
  height: 20px;
}
  &__wrapper {
    display: flex;
    justify-content: space-between;
    gap: 20px;
    flex-wrap: wrap;
    @media screen and (max-width: 1300px) {
       flex-direction: column;
    }
  }
  &__name {
      margin-bottom: 10px;
      color: #000000;
    font-family: 'Akrobat';
    font-size: 20px;
    font-style: normal;
    font-weight: 600;
    @media screen and (max-width: 600px) {
      font-size: 18px;
      text-align: center;
    }
    }
&__card {
  background: #f4f4f4;
    padding: 20px;
    border-radius: 8px;
    width: calc(33.33% - 20px);
    box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
    @media screen and (max-width: 1300px) {
     width: 100%;
    }
}
&__style-link {
  color: #201919;
    font-family: 'Akrobat';
    font-size: 16px;
    font-style: normal;
    font-weight: 400;
}
&__address {
    margin-top: 40px;
    text-align: center;
}
    &__address-title {
      color: #201919;
    font-family: 'Akrobat';
    font-size: 25px;
    font-style: normal;
    font-weight: 700;
      margin-bottom: 15px;
    }

    &__address-text {
      margin-bottom: 5px;
       color: #201919;
    font-family: 'Akrobat';
    font-size: 18px;
    font-style: normal;
    font-weight: 400;
    }
    &__address-link {
      color: #201919;
    font-family: 'Akrobat';
    font-size: 18px;
    font-style: normal;
    font-weight: 400;
    }
}
</style>
