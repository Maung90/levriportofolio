<template>
  <section id="about" class="min-h-screen flex flex-col justify-center pt-20 pb-16 px-5 sm:px-8 relative overflow-hidden">

    <!-- Subtle grid background -->
    <div class="absolute inset-0 bg-[linear-gradient(to_right,#e5e7eb_1px,transparent_1px),linear-gradient(to_bottom,#e5e7eb_1px,transparent_1px)] dark:bg-[linear-gradient(to_right,#1f2937_1px,transparent_1px),linear-gradient(to_bottom,#1f2937_1px,transparent_1px)] bg-[size:4rem_4rem] opacity-40 -z-10"></div>

    <div class="max-w-6xl mx-auto w-full">

      <!-- Label -->
      <div class="mb-6 sm:mb-8" data-aos="fade-up">
        <span class="inline-flex items-center gap-2 text-xs font-semibold tracking-[0.2em] uppercase text-gray-400 dark:text-gray-500">
          <span class="w-6 h-px bg-gray-400 dark:bg-gray-500"></span>
          Web Developer
        </span>
      </div>

      <!-- Main heading -->
      <div class="mb-8 sm:mb-10" data-aos="fade-up" data-aos-delay="100">
        <h1 class="text-5xl sm:text-6xl md:text-7xl lg:text-8xl font-black tracking-tighter leading-[0.9] text-gray-900 dark:text-white">
          HI, I'M<br>
          <div class="h-[1em] overflow-hidden inline-block mt-1">
            <div class="animate-text-slide text-gray-900 dark:text-white">
              <span class="block">LEVRI.</span>
              <span class="block text-gray-400 dark:text-gray-600">DEV.</span>
              <span class="block">LEVRI.</span>
            </div>
          </div>
        </h1>
      </div>

      <!-- Description + CTA row -->
      <div class="flex flex-col sm:flex-row sm:items-end gap-6 sm:gap-12" data-aos="fade-up" data-aos-delay="200">
        <p class="text-gray-500 dark:text-gray-400 leading-relaxed text-base sm:text-lg max-w-md">
          Junior Web Developer dengan fondasi kuat di ekosistem PHP (Laravel/CodeIgniter), antusias membangun arsitektur backend modern menggunakan Go & Python.
        </p>

        <div class="flex flex-col xs:flex-row gap-3 shrink-0">
          <a
            href="/docs/cv-levri.pdf"
            class="inline-flex items-center gap-2 bg-gray-900 dark:bg-white text-white dark:text-black px-6 py-3 text-sm font-bold tracking-wide uppercase hover:bg-gray-700 dark:hover:bg-gray-100 transition-colors duration-200"
          >
            Download CV
            <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="2" stroke="currentColor" class="w-4 h-4">
              <path stroke-linecap="round" stroke-linejoin="round" d="M3 16.5v2.25A2.25 2.25 0 0 0 5.25 21h13.5A2.25 2.25 0 0 0 21 18.75V16.5M16.5 12 12 16.5m0 0L7.5 12m4.5 4.5V3" />
            </svg>
          </a>
          <a
            href="#project"
            class="inline-flex items-center gap-2 border border-gray-300 dark:border-gray-700 text-gray-700 dark:text-gray-300 px-6 py-3 text-sm font-bold tracking-wide uppercase hover:border-gray-900 dark:hover:border-gray-400 hover:text-gray-900 dark:hover:text-white transition-colors duration-200"
          >
            View Work
          </a>
        </div>
      </div>

      <!-- Bottom stats row -->
      <div class="mt-16 sm:mt-20 pt-8 border-t border-gray-200 dark:border-gray-800 grid grid-cols-3 gap-4 sm:gap-8 max-w-sm sm:max-w-lg" data-aos="fade-up" data-aos-delay="300">
        <div>
          <p class="text-2xl sm:text-3xl font-black text-gray-900 dark:text-white">4+</p>
          <p class="text-xs text-gray-400 dark:text-gray-500 uppercase tracking-wide mt-1">Projects</p>
        </div>
        <div>
          <p class="text-2xl sm:text-3xl font-black text-gray-900 dark:text-white">2</p>
          <p class="text-xs text-gray-400 dark:text-gray-500 uppercase tracking-wide mt-1">Internships</p>
        </div>
        <div>
          <p class="text-2xl sm:text-3xl font-black text-gray-900 dark:text-white">11+</p>
          <p class="text-xs text-gray-400 dark:text-gray-500 uppercase tracking-wide mt-1">Skills</p>
        </div>
      </div>

    </div>

    <!-- Floating illustration (hidden on small screens) -->
    <div class="hidden lg:block absolute right-8 xl:right-16 top-1/2 -translate-y-1/2 opacity-60 dark:opacity-30">
      <img
        src="/images/undraw/undraw_programming_re_kg9v.svg"
        alt="Coding Illustration"
        class="w-72 xl:w-96 animate-float"
      >
    </div>

  </section>
</template>

<style scoped>
.animate-float {
  animation: float 6s ease-in-out infinite;
}

@keyframes float {
  0%, 100% { transform: translateY(0px); }
  50% { transform: translateY(-16px); }
}

.animate-text-slide {
  animation: slideText 5s infinite cubic-bezier(0.8, 0, 0.2, 1);
}

@keyframes slideText {
  0%, 35% { transform: translateY(0%); }
  50%, 85% { transform: translateY(-33.33%); }
  100% { transform: translateY(0%); }
}
</style>
