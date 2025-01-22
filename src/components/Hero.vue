<template>
    <section class="relative w-full" data-aos="zoom-in-up">
        <div class="absolute tp-0 inset-x-0 h-64 flex items-start">
            <div class="h-24 w-2/3 bg-gradient-to-br from-[#570cac] blur-2xl invisible opacity-40"></div>
            <div class="h-20 w-3/5 bg-gradient-to-r from-[#670ccf] opacity-40 blur-2xl"></div>
        </div>

        <!-- Rimosso mx-64 e modificato i max-width -->
        <div class="w-full px-5 sm:px-8 md:px-12 lg:px-8 max-w-screen-xl mx-auto relative">
            <div class="grid lg:grid-cols-2 gap-10 xl:gap-20 relative pt-24">
                <div class="md:justify-center lg:py-6">
                    <div class="text-center lg:text-left max-w-2xl">
                        <h1 class="pt-4 text-white font-bold text-4xl md:text-5xl lg:text-6xl">
                            Ciao, sono <span
                                class="text-transparent bg-clip-text bg-gradient-to-r from-primary to-pink-500">
                                Johison
                            </span>
                        </h1>
                    </div>
                    <p class="text-gray-300 pt-8 text-center max-w-2xl">
                        Sono un sviluppatore full-stack con una solida esperienza nella realizzazione di applicazioni
                        moderne e scalabili. La mia passione per la programmazione mi spinge a esplorare sempre nuove
                        tecnologie e a creare soluzioni efficienti e di alta qualità. Con una conoscenza approfondita di
                        JavaScript e TypeScript, sono in grado di affrontare progetti complessi sia lato frontend che
                        backend, garantendo un'ottima esperienza utente e un'architettura robusta.
                    </p>
                    <div
                        class="flex w-full justify-center flex-col gap-12 md:gap-16 lg:gap-24 lg:flex-row xl:gap-28 xl:flex-row pt-16">
                        <button class=" border rounded-full px-4 sm:px-6 md:px-8 py-2 sm:py-3 
                                        bg-secondary hover:bg-primary text-white font-bold
                                        transition-all duration-300 ease-in-out
                                        transform hover:scale-105
                                        w-full sm:w-auto">
                            Prenota
                        </button>
                        <a href="/CV.pdf" download="CV.pdf" class="border rounded-full px-4 sm:px-6 md:px-8 py-2 sm:py-3 
                                   bg-secondary hover:bg-primary text-white font-bold
                                   transition-all duration-300 ease-in-out
                                   transform hover:scale-105
                                   w-full sm:w-auto
                                   flex items-center justify-center cursor-pointer">
                            <svg class="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                                    d="M4 16v1a3 3 0 003 3h10a3 3 0 003-3v-1m-4-4l-4 4m0 0l-4-4m4 4V4" />
                            </svg>
                            Scarica il CV
                        </a>
                    </div>
                </div>
                <div class="lg:h-full md:flex justify-center lg:justify-end">
                    <img src="../assets/animated.png" alt="profilo"
                        class="w-full max-w-xl h-auto rounded-full  object-cover" loading="lazy">
                </div>
            </div>
            <!-- Modificato il container dell'immagine per riempire meglio lo spazio -->

        </div>

    </section>
</template>
<script setup>
import AOS from 'aos';
import 'aos/dist/aos';
AOS.init();

</script>