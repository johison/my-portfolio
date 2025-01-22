<script setup>
//import Hero from '@/components/Hero.vue'
import { defineAsyncComponent } from 'vue';

const NavBar = defineAsyncComponent(()=>import('@/components/NavBar.vue'));
const Hero = defineAsyncComponent(()=>import('@/components/Hero.vue'));

</script>

<template>
  <div class="bg-[#111827] min-h-screen">
    <NavBar />
    <Hero />
     
  </div>
</template>

