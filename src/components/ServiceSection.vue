<template>
    <section class="text-white mt-20" id="services">
       <div class="px-4 xl:pl-16">
            <h2 class="text-4xl font-bold text-white mb-4">Miei Servizi</h2>
       </div>
       <div class="py-8 px-4 sm:py-16 grid grid-cols-1 gap-6 pt-10 sm:grid-cols-2 md:gap-10 md:pt-12 md:grid-cols-3">

       </div>
    </section>
</template>

<script setup>
import { ref } from 'vue';

const services = ref ([
    {
        id:1,
        icon:'https://img.icons8.com/ios-filled/100/ffffff/google-code.png',
        name: 'Sviluppo Web',
        description: 'lorem takotktokto dijidjd isijiosp'
    },
    {
        id:2,
        icon:'https://img.icons8.com/external-vectorslab-gylph-vectorslab/1000/ffffff/external-Technical-Writing-mobile-app-development-glyph-vectorslab.png',
        name: 'Technical Writer (Redattore Tecnico)',
        description: 'lorem takotktokto dijidjd isijiosp'
    },
    {
        id:3,
        icon:'https://img.icons8.com/external-solid-design-circle/100/ffffff/external-Mobile-Development-digital-marketing-solid-design-circle.png',
        name: 'Sviluppo Mobile',
        description: 'lorem takotktokto dijidjd isijiosp'
    },
    {
        id:4,
        icon:'https://img.icons8.com/ios-filled/100/ffffff/windows10-personalization.png',
        name: 'Graphic Design',
        description: 'lorem takotktokto dijidjd isijiosp'
    },
    {
        id:5,
        icon:'https://img.icons8.com/ios-filled/100/ffffff/web-design.png',
        name: 'Web Design',
        description: 'lorem takotktokto dijidjd isijiosp'
    }
])
</script>

