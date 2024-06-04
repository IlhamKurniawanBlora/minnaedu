<template>
  <CustomLoading v-if="isLoading"/>
  <div>
    <NuxtLayout>
      <NuxtPage />
    </NuxtLayout>
  </div>
</template>

<script setup>
 import { ref } from 'vue';

const isLoading = ref(true);
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