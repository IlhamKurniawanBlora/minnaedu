<template>
    <section id="tutor-guru" class="bg-gradient-to-br from-red-200 to-teal-300">
        <div class="flex flex-wrap justify-center items-center mx-auto max-w-screen-lg">
          <div class="text-center py-12 ">
              <h2 class="text-base font-bold text-indigo-600">
                Kami memiliki Tutor dan Guru terbaik
              </h2>
              <h1 class="font-bold text-3xl md:text-4xl lg:text-5xl font-heading text-gray-900">
                <span class="text-[#FC56A7]">Minna</span> <span class="text-[#99C04A]">Education</span> Guru Dan Tutor <span class="text-[#45B3BA]">Handal</span>
              </h1>
          </div>
        </div>
        <div class="flex flex-wrap justify-center items-center mx-auto max-w-screen-lg pb-12">
            <div class="md:w-1/3 sm:w-1/2 p-4 group" v-for="(guru, index) in gurus" :key="index">
                <div class="card w-full bg-white rounded-lg shadow-lg overflow-hidden relative">
                <div class="w-full h-80">
                    <img class="object-center object-cover w-full h-full group-hover:scale-110 duration-300 ease-in cursor-pointer delay-100" :src="guru.img" :alt="guru.alt">
                </div>
                <div class="overlay absolute inset-0 bg-black bg-opacity-50 text-white flex flex-col justify-center items-center transform translate-y-full opacity-0">
                    <h2 class="text-xl font-bold mb-1">{{ guru.nama }}</h2>
                    <p class="text-base text-semibold mb-4">
                    {{ guru.peran }}
                    </p>
                    <div class="flex space-x-4">
                    <a :href="guru.linkfacebook" class="w-8 h-8 bg-gray-800 rounded-full flex items-center justify-center">
                        <LogoFacebook class="hover:text-blue-500 hover:shadow-blue-400 transition-all ease-in-out duration-300"/>
                    </a>
                    <a :href="guru.linkinstagram" class="w-8 h-8 bg-gray-800 rounded-full flex items-center justify-center">
                        <LogoInstagram class="hover:text-red-500 hover:shadow-red-400 transition-all ease-in-out duration-300"/>
                    </a>
                    <a :href="guru.linkwhatsapp" class="w-8 h-8 bg-gray-800 rounded-full flex items-center justify-center">
                        <LogoWhatsapp class="hover:text-green-500 hover:shadow-green-400 transition-all ease-in-out duration-300"/>
                    </a>
                    </div>
                </div>
                </div>
            </div>
        </div>
    </section>
    
</template>
<style>
    .overlay {
      transition: transform 1s, opacity 1s;
    }
    .card:hover .overlay {
      transform: translateY(0);
      opacity: 1;
    }
  </style>
<script lang="ts" setup>
import { ref } from 'vue';

interface Guru {
  nama: string;
  peran: string;
  linkfacebook: string;
  linkwhatsapp: string;
  linkinstagram: string;
  alt: string;
  img?: string;
}

const gurus = ref<Guru[]>([
  {
    nama: 'Sudarmini S.E.',
    peran: 'Tutors and Teachers',
    linkfacebook: 'https://www.facebook.com/',
    linkwhatsapp: 'https://wa.me/',
    linkinstagram: 'https://www.instagram.com/',
    alt: 'minna education',
    img: '_nuxt/public/images/boy_5.jpg'
  },
  {
    nama: 'Minna Education',
    peran: 'Tutors and Teachers',
    linkfacebook: 'https://www.facebook.com/',
    linkwhatsapp: 'https://wa.me/',
    linkinstagram: 'https://www.instagram.com/',
    alt: 'minna education',
    img: '_nuxt/public/images/boy_3.jpg'
  },
  {
    nama: 'Minna Education',
    peran: 'Tutors and Teachers',
    linkfacebook: 'https://www.facebook.com/',
    linkwhatsapp: 'https://wa.me/',
    linkinstagram: 'https://www.instagram.com/',
    alt: 'minna education',
    img: '_nuxt/public/images/kid_2.jpg'
  },
  {
    nama: 'Minna Education',
    peran: 'Tutors and Teachers',
    linkfacebook: 'https://www.facebook.com/',
    linkwhatsapp: 'https://wa.me/',
    linkinstagram: 'https://www.instagram.com/',
    alt: 'minna education',
    img: '_nuxt/public/images/kid_3.jpg'
  },
  
]);
</script>