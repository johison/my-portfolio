Project Grid Component

<template>
    <section class="text-white mt-20 mb-20" id="projects">
        <div class="px-4 xl:pl-16">
            <div class="mb-4 md:flex md:justify-between xl:pr-16">
                <h2 class="text-4xl font-bold text-white">I Miei Progetti</h2>
                <div class="flex space-x-4 mb-4 mt-5 md:mt-0">
                    <button 
                        v-for="category in ['all', 'Sviluppo Web', 'Sviluppo Mobile']"
                        :key="category"
                        @click="selectedCategory = category"
                        class="hover:text-primary transition-colors"
                        :class="{'text-primary': selectedCategory === category}"
                    >
                        {{ category }}
                    </button>
                </div>
            </div>
            <ul class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-6 pt-10 pb-10" data-aos="fade-right">
                <li v-for="project in filteredProjects" 
                    :key="project.id"
                    class="relative group h-64 rounded-lg border rounded-lg overflow-hidden">
                    <img :src="project.image" 
                         :alt="project.title"
                         class="w-full h-full object-cover" />
                    
                    <div class="absolute inset-0 bg-black bg-opacity-70 opacity-0 group-hover:opacity-100 
                              transition-opacity duration-300 flex flex-col justify-center items-center space-y-4">
                        <h3 class="text-xl font-bold">{{ project.title }}</h3>
                        <p class="text-sm px-4 text-center">{{ project.description }}</p>
                        <div class="flex space-x-4">
                            <a v-if="project.gitURL" 
                               :href="project.gitURL"
                               target="_blank"
                               class="text-white hover:text-primary transition-colors">
                                <i class="fab fa-github text-2xl"></i>
                            </a>
                            <a v-if="project.webURL" 
                               :href="project.webURL"
                               target="_blank"
                               class="text-white hover:text-primary transition-colors">
                                <i class="fas fa-external-link-alt text-2xl"></i>
                            </a>
                        </div>
                        <div class="flex flex-wrap gap-2 px-4">
                            <span v-for="tech in project.technologies" 
                                  :key="tech"
                                  class="text-sm bg-primary bg-opacity-20 px-2 py-1 rounded">
                                {{ tech }}
                            </span>
                        </div>
                    </div>
                </li>
            </ul>
        </div>
    </section>
</template>
<script setup>
import { ref, computed } from 'vue';

const projects = ref([
    {
        id: 1,
        category: 'Sviluppo Web',
        image: 'src/assets/progetto-4.jpg',
        title: 'Progetto 1',
        description: 'descrizione 1',
        technologies: ['vue.js 3', 'vuex', 'express'],
        gitURL: '',
        webURL: ''
    },
    {
        id: 2,
        category: 'Sviluppo Web',
        image: 'src/assets/progetto-2.jpg',
        title: 'Progetto 2',
        description: 'descrizione 2',
        technologies: ['vue.js 3', 'vuex', 'express'],
        gitURL: '',
        webURL: ''
    },
    {
        id: 3,
        category: 'Sviluppo Web',
        image: 'src/assets/progetto-1.jpg',
        title: 'Progetto 3',
        description: 'descrizione 2',
        technologies: ['vue.js 3', 'vuex', 'express'],
        gitURL: '#',
        webURL: '#'
    }
]);

const selectedCategory = ref('all');
const filteredProjects = computed(() => {
    if (selectedCategory.value === 'all') {
        return projects.value;
    }
    return projects.value.filter(project => project.category.toLocaleLowerCase() === selectedCategory.value.toLocaleLowerCase());

})
</script>
