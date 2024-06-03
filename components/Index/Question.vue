<template>
    <div class="w-full py-8 px-16 bg-gradient-to-b from-white to-teal-300 border-b-2 border-black">
      <div class="container mx-auto w-full rounded-2xl transparent p-2 max-w-2xl">
        <div class="max-w-2xl mx-auto text-center mb-3 lg:mb-8">
            <h2 class="text-3xl font-bold leading-tight text-black sm:text-4xl lg:text-5xl">
                Common Questions at <span class="text-[#FC56A7]">Minna</span> <span class="text-[#99C04A]">Education</span>
            </h2>
        </div>
        <Disclosure v-slot="{ open }">
          <DisclosureButton
            class="flex mb-2 w-full justify-between items-center
            border-2 border-red-800 rounded-lg bg-red-100 px-4 py-2 text-left text-sm font-medium text-red-900 hover:bg-red-200 focus:outline-red-800 focus-visible:ring focus-visible:ring-red-500/75
            lg:text-xl"
          >
            <span>Apa saja program yang ditawarkan di Minna Education?</span>
              <span v-show="open" ><LogoDown/></span>
              <span v-show="!open" ><LogoUp/></span>
              
          </DisclosureButton>
          <Transition name="opacity">
          <DisclosurePanel class="px-4 py-4 text-sm text-slate-800 bg-red-100 border-2 border-red-800 rounded-lg mb-2 lg:text-lg">
            Kami menawarkan program pembelajaran tambahan untuk anak-anak PAUD, SD/MI, dan SMP/MTS yang didasarkan pada kurikulum yang berlaku. Program ini mencakup kiat, trik, dan tips dalam mengerjakan soal ujian. Selain itu, kami juga menyelingi pembelajaran dengan mengaji Quran dan pendidikan akhlak.
          </DisclosurePanel>
        </Transition>

        </Disclosure>
        <Disclosure v-slot="{ open }">
          <DisclosureButton
            class="flex mb-2 w-full justify-between items-center
            border-2 border-green-800 rounded-lg bg-green-100 px-4 py-2 text-left text-sm font-medium text-green-900 hover:bg-green-200 focus:outline-green-800 focus-visible:ring focus-visible:ring-green-500/75
            lg:text-xl"
          >
            <span>Bagaimana cara mendaftar untuk program ini?</span>
              <span v-show="open" ><LogoDown/></span>
              <span v-show="!open" ><LogoUp/></span>
              
          </DisclosureButton>
          <Transition name="opacity">
          <DisclosurePanel class="px-4 py-4 text-sm text-slate-800 bg-green-100 border-2 border-green-800 rounded-lg mb-2 lg:text-lg">
            Untuk mendaftarkan anak Anda dalam program ini, cukup klik tombol "Hubungi Kami" atau langsung datang ke tempat les di Minna Education.
          </DisclosurePanel>
        </Transition>

        </Disclosure>
        
        <Disclosure v-slot="{ open }">
          <DisclosureButton
            class="flex mb-2 w-full justify-between items-center
            border-2 border-red-800 rounded-lg bg-red-100 px-4 py-2 text-left text-sm font-medium text-red-900 hover:bg-red-200 focus:outline-red-800 focus-visible:ring focus-visible:ring-red-500/75
            lg:text-xl"
          >
            <span>Siapa saja pengajar di sini dan apa kualifikasi mereka?</span>
              <span v-show="open" ><LogoDown/></span>
              <span v-show="!open" ><LogoUp/></span>
              
          </DisclosureButton>
          <Transition name="opacity">
          <DisclosurePanel class="px-4 py-4 text-sm text-slate-800 bg-red-100 border-2 border-red-800 rounded-lg mb-2 lg:text-lg">
            Pengajar kami adalah tenaga pendidik yang berpengalaman dan memiliki latar belakang pendidikan yang sesuai, baik dari perguruan tinggi maupun pesantren. Mereka juga memiliki sertifikasi mengajar yang relevan.
          </DisclosurePanel>
        </Transition>

        </Disclosure>
        <Disclosure v-slot="{ open }">
          <DisclosureButton
            class="flex mb-2 w-full justify-between items-center
            border-2 border-green-800 rounded-lg bg-green-100 px-4 py-2 text-left text-sm font-medium text-green-900 hover:bg-green-200 focus:outline-green-800 focus-visible:ring focus-visible:ring-green-500/75
            lg:text-xl"
          >
            <span>Apakah ada sesi konsultasi untuk orang tua?</span>
              <span v-show="open" ><LogoDown/></span>
              <span v-show="!open" ><LogoUp/></span>
              
          </DisclosureButton>
          <Transition name="opacity">
          <DisclosurePanel class="px-4 py-4 text-sm text-slate-800 bg-green-100 border-2 border-green-800 rounded-lg mb-2 lg:text-lg">
            Kami sangat menghargai peran orang tua dalam pendidikan anak. Oleh karena itu, kami menyediakan sesi konsultasi rutin untuk orang tua agar dapat berdiskusi langsung dengan pengajar mengenai perkembangan anak.
          </DisclosurePanel>
        </Transition>

        </Disclosure>
        

        
        
      </div>
    </div>
  </template>
  <style>
  .opacity-enter-active, .opacity-leave-active {
  transition: opacity 0.3s;
}
.opacity-enter-from, .opacity-leave-to {
  opacity: 0;
}
  </style>
  <script setup>
  import { Disclosure, DisclosureButton, DisclosurePanel } from '@headlessui/vue';
  import { ChevronUpIcon, ChevronDownIcon } from '@heroicons/vue/20/solid';
  </script>