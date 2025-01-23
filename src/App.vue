<script setup>
//import Hero from '@/components/Hero.vue'
import { defineAsyncComponent } from 'vue';
import LoadingSpinner from './components/LoadingSpinner.vue';

const NavBar = defineAsyncComponent(()=>import('@/components/NavBar.vue'));
const Hero = defineAsyncComponent(()=>import('@/components/Hero.vue'));
const ServiceSection = defineAsyncComponent(()=>import('@/components/ServiceSection.vue'));
const AboutSection = defineAsyncComponent(()=>import('@/components/AboutSection.vue'));
const ExperienceAndSkills = defineAsyncComponent(()=>import('@/components/ExperienceAndSkills.vue'));
const Projects = defineAsyncComponent(()=>import('@/components/Projects.vue'));
const ContactSection = defineAsyncComponent(()=>import('@/components/ContactSection.vue'));
const FooterSection = defineAsyncComponent(()=>import('@/components/Footer.vue'));
const BackToTop = defineAsyncComponent(()=>import('@/components/BackToTop.vue'));



</script>

<template>
  <div class="bg-[#111827] min-h-screen">
    <!--raggruppo i componenti in suspense per gestire il loading-->
  <Suspense>
    <template #default>
      <!-- raggruppo i componenti in una singola root elemento-->
      <div>
        <NavBar />
        <Hero />
        <ServiceSection />
        <AboutSection />
        <ExperienceAndSkills />
        <Projects />
        <ContactSection />
        <FooterSection />
        <BackToTop />
      </div>
    </template>
    <template #fallback>
      <div class="flex justify-center items-center min-h-screen">
        <LoadingSpinner />
      </div>
    </template>
  </Suspense>    
  </div>
</template>

<style scoped>
*{
  scrollbar-width: thin;
  scrollbar-color: #111827 #f1f1f1
}
</style>

