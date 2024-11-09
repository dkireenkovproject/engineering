<template>
  <div class="PopUp">
    <div class="container">
      <div class="PopUp__Wrapper" @click="$emit('close-form')">
        <div class="PopUp__card" @click.stop>
          <span class="PopUp__title">Наши контакты</span>
          <img @click="$emit('close-form')" src="/img/close.svg" class="PopUp__img-close" alt="close" />

          <div v-for="(contact, index) in contacts" :key="index" class="PopUp__contact">
            <span class="PopUp__contact-name">{{ contact.name }}</span>
            <span class="PopUp__contact-position">{{ contact.position }}</span>
            <div class="PopUp__contact-wrapper"><img class="PopUp__img" :src="contact.img1" alt="img"><a :href="'mailto:' + contact.email" class="PopUp__contact-email">{{ contact.email }}</a></div> 
            <div class="PopUp__contact-wrapper"><img class="PopUp__img" :src="contact.img2" alt="img"><a :href="'tel:' + contact.phone.replace(/[^0-9]/g, '')" class="PopUp__contact-phone">{{ contact.phone }}</a></div> 
          </div>
          
        </div>
      </div>
    </div>
  </div>
</template>

<script setup lang="ts">
const contacts = [
  {
    name: "Алексей Баранов",
    position: "Генеральный директор",
    email: "alebar@b3-d.ru",
    phone: "+7 (925) 391-6402",
    img1: "/img/mail.png",
    img2: "/img/telephone.png",
  },
  {
    name: "Подольский Александр",
    position: "Руководитель проектов",
    email: "alepod@b3-d.ru",
    phone: "+7 (926) 503-3953",
    img1: "/img/mail.png",
    img2: "/img/telephone.png",
  },
  {
    name: "Маргарита Тарасова",
    position: "Директор по развитию",
    email: "martar@b3-d.ru",
    phone: "+7 (925) 554-6959",
    img1: "/img/mail.png",
    img2: "/img/telephone.png",
  },
];
</script>

<style scoped lang="scss">
.PopUp {
  &__Wrapper {
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    height: 100vh;
    z-index: 99998;
    background-color: rgba(0, 0, 0, 0.3);
    display: grid;
    align-items: center;
    justify-content: center;
    overflow-y: auto;
  }

  &__card {
    position: relative;
    display: flex;
    flex-direction: column;
    align-items: center;
    margin: 30px 15px;
    min-width: 500px;
height: auto;
    padding: 45px;
    z-index: 1;
    background-color: #e4e7eb;
    box-shadow: 0px 0px 17px -7px rgba(34, 60, 80, 0.2);
    border-radius: 30px;
  }
&__contact-wrapper {
  display: flex;
  align-items: center;
  gap: 5px;
}
&__img {
  width: 20px;
  height: 20px;
  }
  &__img-close {
    position: absolute;
    cursor: pointer;
    top: 17px;
    right: 17px;
    width: 20px;
    height: 20px;
  }

  &__title {
    margin-bottom: 30px;
    color: #000;
    font-family: 'Akrobat', sans-serif;
    font-size: 40px;
    font-weight: 700;
  }

  &__contact {
    display: flex;
    flex-direction: column;
    background-color: #fff;
    padding: 20px;
    margin-bottom: 15px;
    width: 100%;
    border-radius: 15px;
    box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1);

    &-name {
      font-size: 18px;
      font-family: 'Akrobat';
      font-weight: 600;
      margin-bottom: 5px;
      font-style: normal;
    }

    &-position {
      margin-bottom: 10px;
      font-family: 'Akrobat';
      font-size: 14px;
      font-style: normal;
      font-weight: 400;
      color: #666;
    }

    &-email, &-phone {
      color: #201919;
    font-family: 'Akrobat';
    font-size: 16px;
    font-style: normal;
    font-weight: 400;
    }
  }
}
</style>
