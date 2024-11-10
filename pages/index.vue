<template>
  <div class="home-background">
    <HeaderLayout />
    <HomeHero />
    <HomeServices />
    <HomeProject />
    <HomeContacts />
    <FooterLayout />
  </div>
</template>

<script lang="ts" setup>

</script>

<style lang="scss" scoped>
.home-background {
  background-image: url('img/home-bg.jpg'); 
  background-size: cover;
  background-repeat: no-repeat;
  background-attachment: fixed; /* Фиксируем фон */
  background-position: center center;
}
</style>