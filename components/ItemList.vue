<template>
    <div>
      <ul class="flex justify-start">
        <li v-for="(item, index) in items" :key="index">
            <a class="block px-6 py-6 transition whitespace-nowrap hover:text-indigo-500" 
            :href="item.href">{{ item.label }}</a>
        </li>
        </ul>
    </div>
  </template>
  
  <script lang="ts" setup>
  import { defineProps } from 'vue';
  
  interface Item {
    label: string;
    href: string;
  }
  
  const props = defineProps<{
    items: Item[]
  }>();
  </script>