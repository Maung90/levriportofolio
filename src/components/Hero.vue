<template>
  <section id="about" class="min-h-screen flex items-center justify-center py-20 px-4 sm:px-6 lg:px-8 overflow-hidden relative">

    <div class="absolute top-20 right-20 w-72 h-72 bg-primary/10 rounded-full blur-3xl -z-10"></div>

    <div class="max-w-7xl w-full grid grid-cols-1 lg:grid-cols-2 gap-12 items-center">

      <div class="order-2 lg:order-1" data-aos="fade-right">
        <small class="text-gray-500 dark:text-gray-400 text-lg block mb-2">Welcome to <span class="font-semibold text-gray-800 dark:text-gray-200">my portfolio website!</span></small>

        <h1 class="text-4xl md:text-6xl font-bold mb-6 flex align-center md:flex-row md:items-center gap-2 md:gap-4">
          <span class="mr-2">Hi, I'm</span>

          <div class="h-[1.2em] overflow-hidden inline-block align-middle relative text-primary">
            <div class="animate-text-slide">
              <span class="block h-full">Levri</span>
              <span class="block h-full">Junior Web Developer</span>
              <span class="block h-full">Levri</span>
            </div>
          </div>
        </h1>

        <p class="text-gray-600 dark:text-gray-300 leading-relaxed text-lg mb-8 max-w-lg">
          Junior Web Developer yang memiliki fondasi kuat dalam ekosistem PHP (Laravel/CodeIgniter). Memiliki antusiasme tinggi dalam mempelajari teknologi backend modern seperti Go (Golang) dan Python untuk membangun arsitektur aplikasi yang handal dan aman.
        </p>

        <div class="flex gap-4">
          <a href="/docs/cvats.pdf" class="bg-gray-900 dark:bg-white text-white dark:text-gray-900 px-8 py-3 rounded-full font-semibold shadow-lg hover:shadow-xl hover:-translate-y-1 transition-all duration-300">
            Download cv
          </a>
        </div>
      </div>

      <div class="order-1 lg:order-2 flex justify-center" data-aos="fade-left">
        <img src="/images/undraw/undraw_programming_re_kg9v.svg" alt="Coding Illustration" class="w-full max-w-md drop-shadow-2xl animate-float">
      </div>
    </div>
  </section>
</template>

<style scoped>
.animate-float {
  animation: float 6s ease-in-out infinite;
}

@keyframes float {
  0% { transform: translateY(0px); }
  50% { transform: translateY(-20px); }
  100% { transform: translateY(0px); }
}

.animate-text-slide {
  animation: slideText 6s infinite cubic-bezier(0.8, 0, 0.2, 1);
}

@keyframes slideText {
  0%, 20% {
    transform: translateY(0%);
  }
  33%, 53% {
    transform: translateY(-100%);
  }
  66%, 86% {
    transform: translateY(-200%);
  }
  100% {
    transform: translateY(0%);
  }
}
</style>
