<script setup>
import { onMounted } from 'vue';
import Navbar from './components/Navbar.vue';
import Hero from './components/Hero.vue';
import Projects from './components/Projects.vue';
import Experience from './components/Experience.vue';
import Skills from './components/Skills.vue';
import Footer from './components/Footer.vue';
import AOS from 'aos';
import 'aos/dist/aos.css';

onMounted(() => {
  AOS.init({
    duration: 800,
    once: true,
    easing: 'ease-out-cubic',
  });
});
</script>

<template>
  <div class="bg-white dark:bg-black text-gray-900 dark:text-gray-100 transition-colors duration-300 min-h-screen overflow-x-hidden selection:bg-black selection:text-white dark:selection:bg-white dark:selection:text-black">
    <Navbar />
    <main>
      <Hero />
      <Projects />
      <Experience />
      <Skills />
    </main>
    <Footer />
  </div>
</template>
