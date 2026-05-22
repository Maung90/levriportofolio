<script setup>
const skills = [
  { name: 'PHP', img: '/images/icon/php.svg', color: '#777BB4' },
  { name: 'JavaScript', img: '/images/icon/javascript.svg', color: '#F7DF1E' },
  { name: 'Bootstrap', img: '/images/icon/bootstrap.svg', color: '#7952B3' },
  { name: 'Tailwind CSS', img: '/images/icon/tailwind.svg', color: '#38B2AC' },
  { name: 'Laravel', img: '/images/icon/laravel.svg', color: '#FF2D20' },
  { name: 'CodeIgniter', img: '/images/icon/codeigniter.svg', color: '#EF4223' },
  { name: 'Golang', img: '/images/icon/Go.svg', color: '#00ACD7' },
  { name: 'Python', img: '/images/icon/python.svg', color: '#3776AB' },
  { name: 'MySQL', img: '/images/icon/mysql.svg', color: '#4479A1' },
  { name: 'Git', img: '/images/icon/git.svg', color: '#F05032' },
  { name: 'API', img: '/images/icon/api.svg', color: '#FF4F00' },
];
</script>

<template>
  <section id="skill" class="py-20 sm:py-28 px-5 sm:px-8 bg-gray-50 dark:bg-gray-950 transition-colors">
    <div class="max-w-6xl mx-auto">

      <!-- Section header -->
      <div class="flex flex-col sm:flex-row sm:items-end justify-between mb-12 sm:mb-16 gap-4" data-aos="fade-up">
        <div>
          <span class="text-xs font-semibold tracking-[0.2em] uppercase text-gray-400 dark:text-gray-500">Toolbox</span>
          <h2 class="text-4xl sm:text-5xl font-black tracking-tighter text-gray-900 dark:text-white mt-2">
            Tech Stack
          </h2>
        </div>
        <p class="text-gray-400 dark:text-gray-500 text-sm max-w-xs sm:text-right">
          Teknologi & tools yang saya kuasai
        </p>
      </div>

      <!-- Skills grid -->
      <div class="grid grid-cols-3 sm:grid-cols-4 md:grid-cols-5 lg:grid-cols-6 gap-px bg-gray-200 dark:bg-gray-800 border border-gray-200 dark:border-gray-800">
        <div
          v-for="(skill, index) in skills"
          :key="index"
          class="group flex flex-col items-center justify-center gap-3 p-5 sm:p-6 bg-white dark:bg-black hover:bg-gray-50 dark:hover:bg-gray-950 transition-colors duration-200 cursor-default"
          data-aos="fade-up"
          :data-aos-delay="index * 40"
        >
          <!-- Icon -->
          <div
            class="w-9 h-9 sm:w-11 sm:h-11 transition-transform duration-300 group-hover:-translate-y-1 group-hover:scale-110"
            :style="{
              backgroundColor: skill.color,
              maskImage: `url(${skill.img})`,
              maskRepeat: 'no-repeat',
              maskPosition: 'center',
              maskSize: 'contain',
              webkitMaskImage: `url(${skill.img})`,
              webkitMaskRepeat: 'no-repeat',
              webkitMaskPosition: 'center',
              webkitMaskSize: 'contain'
            }"
          ></div>

          <!-- Name -->
          <span class="text-xs font-semibold text-gray-500 dark:text-gray-400 group-hover:text-gray-900 dark:group-hover:text-white transition-colors text-center leading-tight">
            {{ skill.name }}
          </span>
        </div>

        <!-- Filler cell to keep grid even if needed (optional visual) -->
      </div>

    </div>
  </section>
</template>
