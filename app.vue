<template>
	<CommonLoadPage v-if="loading" />
	<NuxtLayout v-else>
		<NuxtPage />
	</NuxtLayout>
</template>
<script setup lang="ts">
import { ref, onMounted } from 'vue';

const loading = ref(true);

onMounted(() => {
  setTimeout(() => {
    loading.value = false;
  }, 2000);
});
</script>

<style lang="scss" scoped>
.fade-enter-active, .fade-leave-active {
  transition: opacity 0.5s ease;
}
.fade-enter, .fade-leave-to {
  opacity: 0;
}
</style>