<template>
  <Transition name="fade">
    <CustomLoading v-if="isLoading"/>
  </Transition>
  <div>
    <NuxtLayout>
      <NuxtPage />
    </NuxtLayout>
  </div>
</template>
<style>
html {
  scroll-behavior: smooth;
}
.fade-enter-active, .fade-leave-active {
  transition: opacity 0.5s ease;
}

.fade-enter-from, .fade-leave-to {
  opacity: 0;
}
</style>
<script setup>
 import { ref } from 'vue';

const isLoading = ref(true);
setTimeout(() => {
  loading.value = false;
}, 2000);
useHead({
  title: 'Minna Education | Learning Center ',
  meta: [
    { name: 'description', content: 'Minna Education | Wado, Kedungtuban, Blora, Jawa Tengah' }
  ],
  script: [ { innerHTML: 'console.log(\'Minna Education\')' } ]
});
useSeoMeta({
  title: 'Program Les Terbaik di Kedungtuban - Minna Education',
  ogTitle: 'Program Les Terbaik di Kedungtuban - Minna Education',
  description: 'Gabunglah dengan Minna Education untuk program les terbaik di Kedungtuban. Kami menawarkan pembelajaran tambahan untuk anak-anak PAUD, SD/MI, dan SMP/MTS dengan metode yang efektif dan interaktif.',
  ogDescription: 'Gabunglah dengan Minna Education untuk program les terbaik di Kedungtuban. Kami menawarkan pembelajaran tambahan untuk anak-anak PAUD, SD/MI, dan SMP/MTS dengan metode yang efektif dan interaktif.',
  ogImage: 'https://example.com/image.png',
  twitterCard: 'summary_large_image',
});
</script>