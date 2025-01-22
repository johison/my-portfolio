<template>
    <section class="text-white mt-20" id="services">
       <div class="px-4 xl:pl-16">
            <h2 class="text-4xl font-bold text-white mb-4">Miei Servizi</h2>
       </div>
       <div class="py-8 px-4 sm:py-16 grid grid-cols-1 gap-6 pt-10 sm:grid-cols-2 md:gap-10 md:pt-12 md:grid-cols-3">
         <div v-for="service in services" :key="service.id" data-aos="fade-up"
         class="px-8 py-12 rounded-xl bg-[#111a3e] shadow-lg border border-[#1f1641]">
            <div class="mx-auto h-auto text-center xl:h-auto xl:w-auto">
                <div class="flex justify-center">
                    <img :src="service.icon" alt="service icon">
                </div>
                <div class="text-center group">
                    <h3 class="pt-8 text-lg font-semibold uppercase text-transparent bg-clip-text bg-gradient-to-r from-primary to-secondary lg:text-xl">
                        {{ service.name }}
                    </h3>
                    <p class="text-grey-600 pt-4 text-sm group-hover:text-white md:text-base">
                        {{ service.description }}
                    </p>
                </div>
            </div>
         </div>
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
        description: 'Siti web moderni, responsive e ottimizzati per performance elevate e con tecnologie avanzate per una "esperienza utente impeccabile".'
    },
    {
        id:2,
        icon:'https://img.icons8.com/ios-filled/100/ffffff/pencil.png',
        name: 'Technical Writer (Redattore Tecnico)',
        description: "Creazione di documentazione chiara e precisa, dai manuali alle guide, per facilitare l'uso dei tuoi prodotti e servizi."
    },
    {
        id:3,
        icon:'https://img.icons8.com/ios-filled/100/ffffff/android.png',
        name: 'Sviluppo Mobile',
        description: 'App mobile intuitive e performanti per iOS e Android, con design accattivanti e funzionalità avanzate.'
    },
    {
        id:4,
        icon:'https://img.icons8.com/ios-filled/100/ffffff/windows10-personalization.png',
        name: 'Graphic Design',
        description: 'Design grafico creativo per branding, loghi e materiali promozionali, che comunica visivamente il tuo messaggio in modo efficace.'
    },
    {
        id:5,
        icon:'https://img.icons8.com/ios-filled/100/ffffff/web-design.png',
        name: 'Web Design',
        description: 'Progettazione di interfacce user-friendly, estetiche e responsive per siti web che si adattano a qualsiasi dispositivo.'
    },
    {
        id:6,
        icon:'https://img.icons8.com/ios-filled/100/ffffff/speed.png',
        name: 'SEO',
        description: 'Ottimizzazione per i motori di ricerca (SEO) per migliorare il posizionamento online, incrementando il traffico organico e la visibilità del sito.'
    }
])
</script>

