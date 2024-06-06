<template>
  <div class="flex min-h-screen items-center justify-center bg-gray-100" v-if="isLoading" id="loading-container">
  <div class="container loading-container absolute max-w-[36px] mx-16 rounded p-8 before::sm:max-w-[24px] before::md:max-w-[32px] before::lg:max-w-[40px] before::xl:max-w-[48px] before::2xl:max-w-[56px] sm:max-w-sm md:max-w-md font-bold">
    <div class="loading-text flex justify-center drop-shadow-xl shadow-[#FC56A7] text-[#FC56A7]">
      <span class="loading-letter">M</span>
      <span class="loading-letter">I</span>
      <span class="loading-letter">N</span>
      <span class="loading-letter">N</span>
      <span class="loading-letter">A</span>
    </div>
    <div class="loading-text flex justify-center drop-shadow-xl shadow-[#99C04A] text-[#99C04A]">
      <span class="loading-letter">E</span>
      <span class="loading-letter">D</span>
      <span class="loading-letter">U</span>
      <span class="loading-letter">C</span>
      <span class="loading-letter">A</span>
      <span class="loading-letter">T</span>
      <span class="loading-letter">I</span>
      <span class="loading-letter">O</span>
      <span class="loading-letter">N</span>
    </div>
  </div>
</div>
</template>
<script setup>
import { ref, onMounted, onUnmounted } from 'vue';
import { useRouter } from 'nuxt/app';

const isLoading = ref(true);
const router = useRouter();
const loadingElement = ref(null); // Ref to hold the loading element

function disableScroll() {
  document.body.style.overflow = 'hidden';
}

function enableScroll() {
  document.body.style.overflow = 'auto';
}

function startLoading() {
  disableScroll();
  isLoading.value = true;

  setTimeout(() => {
    isLoading.value = false;
    enableScroll();
    router.push('/')
      .catch((error) => {
        console.error('Navigation error:', error);
      });
  }, 6000);
}

onMounted(() => {
  loadingElement.value = document.querySelector('#loading-container');
  startLoading();
});

onUnmounted(() => {
  enableScroll(); // Ensure scrolling is enabled when the component is unmounted
});
</script>
