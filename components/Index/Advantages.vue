<template>
    <div class="px-3 md:px-40 border-t border-b py-20 bg-opacity-10" style="background-image: url('https://www.toptal.com/designers/subtlepatterns/uploads/dot-grid.png')">
      <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-4 bg-transparent shadow-xl shadow-neutral-100">

        <div class="p-10 flex flex-col items-center text-center group border md:border-r lg:border-b hover:bg-slate-50 cursor-pointer" v-for="(advantage, index) in advantages" :key="index">
          <component :is="componentsMap[advantage.component]"/>
          <h2 class="text-xl font-medium text-slate-700 mt-3">{{ advantage.judul }}</h2>
          <p class="mt-2 text-sm text-slate-500">{{ advantage.deskripsi }}</p>
        </div>

      </div>
  
      <div class="w-full px-6 bg-green-500 shadow-xl shadow-green-200 py-10 sm:py-4 sm:px-2 md:px-10 xl:px-16 lg:px-20 flex justify-between items-center mt-10">
        <p class="text-slate-200">
          <span class="lg:text-4xl md:text-3xl sm:text-2xl font-medium text-indigo-800">Masih Bimbang?</span>
          <br>
          <span class="text-lg">Silahkan Konsultasi untuk kebutuhan Les-lesan anak anda!!</span>
        </p>
        <a href="https://api.whatsapp.com/send?phone=6287764848768" class="px-5 py-3 font-medium text-slate-700 shadow-xl hover:bg-yellow-500 hover:shadow-yellow-200 transition-all duration-150 bg-yellow-400">Konsultasi</a>
      </div>
    </div>
  </template>
  
  <script lang="ts" setup>
  import { ref } from 'vue';
  import LogoAdvantages1 from '@/components/Logo/Advantages1.vue';
  import LogoAdvantages2 from '@/components/Logo/Advantages2.vue';
  import LogoAdvantages3 from '@/components/Logo/Advantages3.vue';
  import LogoAdvantages4 from '@/components/Logo/Advantages4.vue';
  import LogoAdvantages5 from '@/components/Logo/Advantages5.vue';
  import LogoAdvantages6 from '@/components/Logo/Advantages6.vue';
  
  const componentsMap = {
  LogoAdvantages1,
  LogoAdvantages2,
  LogoAdvantages3,
  LogoAdvantages4,
  LogoAdvantages5,
  LogoAdvantages6
};

  interface Advantage {
    judul: string;
    component: string;
    deskripsi: string;
  }
  
  const advantages = ref<Advantage[]>([
    {
      judul: 'Tutor Paling Berpengalaman',
      component: 'LogoAdvantages1',
      deskripsi: 'Tutor berpengalaman berkomitmen pada keunggulan akademik dan nilai-nilai Islam.',
    },
    {
      judul: 'Persiapan Ujian Terbaik',
      component: 'LogoAdvantages2',
      deskripsi: 'Kiat dan strategi praktis untuk kinerja ujian yang percaya diri.',
    },
    {
      judul: 'Integrasi Kurikulum dan Keagamaan',
      component: 'LogoAdvantages3',
      deskripsi: 'Menggabungkan mata pelajaran akademis dengan studi Islam untuk pertumbuhan intelektual dan spiritual.',
    },
    {
      judul: 'Pembelajaran Personalisasi Terbaik',
      component: 'LogoAdvantages4',
      deskripsi: 'Metode pengajaran yang disesuaikan untuk memenuhi kebutuhan individu siswa.',
    },
    {
      judul: 'Pembelajaran Personalisasi Terbaik',
      component: 'LogoAdvantages5',
      deskripsi: 'Metode pengajaran yang disesuaikan untuk memenuhi kebutuhan individu siswa.',
    },
    {
      judul: 'Perkembangan Moral dan Etika',
      component: 'LogoAdvantages6',
      deskripsi: 'Penekanan pada pembentukan karakter dan Akhlakul karimah.',
    }
    
  ]);
  </script>
  