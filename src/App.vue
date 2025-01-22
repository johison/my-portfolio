<script setup>
//import Hero from '@/components/Hero.vue'
import { defineAsyncComponent } from 'vue';

const NavBar = defineAsyncComponent(()=>import('@/components/NavBar.vue'));
const Hero = defineAsyncComponent(()=>import('@/components/Hero.vue'));
const ServiceSection = defineAsyncComponent(()=>import('@/components/ServiceSection.vue'));
const AboutSection = defineAsyncComponent(()=>import('@/components/AboutSection.vue'));
const ExperienceAndSkills = defineAsyncComponent(()=>import('@/components/ExperienceAndSkills.vue'));


</script>

<template>
  <div class="bg-[#111827] min-h-screen">
    <NavBar />
    <Hero />
    <ServiceSection />
    <AboutSection />
    <ExperienceAndSkills />
     
  </div>
</template>

