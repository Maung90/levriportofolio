<script setup>
import { onMounted } from 'vue';
import Navbar from './components/Navbar.vue';
import Hero from './components/Hero.vue';
import Projects from './components/Projects.vue';
import Experience from './components/Experience.vue';
import Skills from './components/Skills.vue';
import Footer from './components/Footer.vue';
// import CustomCursor from './components/CustomCursor.vue';
import AOS from 'aos';
import 'aos/dist/aos.css';

onMounted(() => {
  AOS.init({
    duration: 1000,
    once: true,
  });

});
</script>

<template>
  <div class="bg-white dark:bg-gray-900 text-gray-800 dark:text-gray-200 transition-colors duration-300 min-h-screen overflow-x-hidden selection:bg-primary selection:text-white">

    <!-- <CustomCursor /> -->

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
