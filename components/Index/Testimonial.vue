<template>
	<section id="testimonial" class="bg-neutral-950 bg-opacity-80 border-t-[5px] border-black">
  <div class="max-w-5xl mx-auto w-full px-10 py-10">
    <div class="flex items-center justify-center flex-col gap-y-2 py-5">
      <h2 class="text-2xl md:text-3xl lg:text-4xl font-bold max-w-md mx-auto text-center text-white">Tanggapan
        <span class="text-[#45B3BA]">OrangTua</span> Murid di <span class="text-[#FC56A7]">Minna</span> <span class="text-[#99C04A]">Education</span>
      </h2>
      <p class="text-lg font-medium text-slate-400/70">"Fun Learning and Smart Thinking"</p>
    </div>

    
    <div class="grid grid-cols-1 lg:grid-cols-5 gap-5 w-full">

      <div :class="[getClass(index),'border p-7 rounded-xl bg-neutral-900 drop-shadow-md border-neutral-800/50 flex flex-col gap-y-10 justify-between']" v-for="(ortu, index) in ortus" :key="index">
        <div class="flex flex-col gap-y-3.5">
          <p class="font-bold text-xl text-white">{{ ortu.judul }}</p>
          <p class="font-medium text-white">“{{ ortu.komentar }}”</p>
        </div>
        <div class="flex flex-col"><img :src="ortu.img" :alt="ortu.alt" class="h-10 w-10" >
          <p class="pt-2 text-sm font-semibold text-white">{{ ortu.nama }}</p>
          <p class="text-sm font-medium text-slate-100/70">{{ ortu.ortu }}</p>
        </div>
      </div>
    </div>
  </div>
  </section>

<svg class="" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1440 320"><path fill="#0A0A0A" fill-opacity="0.8" d="M0,160L60,165.3C120,171,240,181,360,176C480,171,600,149,720,128C840,107,960,85,1080,90.7C1200,96,1320,128,1380,144L1440,160L1440,0L1380,0C1320,0,1200,0,1080,0C960,0,840,0,720,0C600,0,480,0,360,0C240,0,120,0,60,0L0,0Z"></path></svg>
</template>

<script lang="ts" setup>
import { ref } from 'vue';

interface Ortu {
  nama: string;
  ortu: string;
  judul: string;
  komentar: string;
  alt: string;
  img?: string;
}

const ortus = ref<Ortu[]>([
  {
    nama: 'Lilis Suliyanti',
    ortu: 'Ibu adinda Asfiya',
    judul: 'Peningkatan Akademik',
    komentar: 'Minna Education telah membantu anak saya meningkatkan nilai akademisnya. Saya telah melihat kemajuan yang signifikan.',
    alt: 'Lilis Suliyanti',
    img: '_nuxt/public/images/boy_1.jpg'
  },
  {
    nama: 'Sulaiman Rahman',
    ortu: 'Ayah Adinda Rina',
    judul: 'Peningkatan Kepercayaan Diri',
    komentar: 'Pelajaran yang diberikan sangat membantu anak saya memahami mata pelajaran sekolah. Anak saya sekarang lebih percaya diri dalam menghadapi ujian.',
    alt: 'Ayah Adinda Rina',
    img: '_nuxt/public/images/boy_2.jpg'
  },
  {
    nama: 'Rosmary',
    ortu: 'Bunda ananda Farhan',
    judul: 'Pembelajaran Komprehensif',
    komentar: 'Saya sangat senang dengan pendekatan yang dilakukan Minna Education. Anak saya tidak hanya mempelajari mata pelajaran umum tetapi juga nilai-nilai agama Islam.',
    alt: 'Bunda ananda Farhan',
    img: '_nuxt/public/images/girl_1.jpg'
  },
  {
    nama: 'Janaka Soleh',
    ortu: 'Ayah ananda Zaki',
    judul: 'Metode Interaktif dan Menyenangkan',
    komentar: 'Anak saya menikmati setiap sesi pembelajaran di Minna Education. Metode pengajarannya interaktif dan menyenangkan.',
    alt: 'Ayah ananda Zaki',
    img: '_nuxt/public/images/boy_3.jpg'
  }  
]);

// Fungsi untuk menentukan kelas berdasarkan index
const getClass = (index: number) => {
  if (index === 1 || index === 2) {
    return 'lg:col-span-3'; // Kelas khusus untuk elemen 2 dan 3
  }
  return 'col-span-2'; // Kelas standar untuk elemen lainnya
};
</script>