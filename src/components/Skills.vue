<script setup>
const skills = [
  { name: 'HTML5', img: '/images/icon/html.svg', color: '#E34F26' },
  { name: 'CSS3', img: '/images/icon/css3.svg', color: '#1572B6' },
  { name: 'PHP', img: '/images/icon/php.svg', color: '#777BB4' },
  { name: 'JavaScript', img: '/images/icon/javascript.svg', color: '#F7DF1E' },
  { name: 'Bootstrap', img: '/images/icon/bootstrap.svg', color: '#7952B3' },
  { name: 'Laravel', img: '/images/icon/laravel.svg', color: '#FF2D20' },
  { name: 'CodeIgniter', img: '/images/icon/codeigniter.svg', color: '#EF4223' },
  { name: 'Python', img: '/images/icon/python.svg', color: '#3776AB' },
  { name: 'MySql', img: '/images/icon/mysql.svg', color: '#4479A1' },
  { name: 'Git', img: '/images/icon/git.svg', color: '#F05032' },
  { name: 'Tailwind CSS', img: '/images/icon/tailwind.svg', color: '#38B2AC' },
  { name: 'Api', img: '/images/icon/api.svg', color: '#FF4F00' },
];
</script>

<template>
  <section id="skill" class="py-20 bg-gray-50 dark:bg-gray-800 transition-colors">
    <div class="container mx-auto px-4 text-center">
      <h2 class="text-3xl font-bold mb-12 text-gray-900 dark:text-white" data-aos="fade-down">Technical Skills</h2>

      <div class="grid grid-cols-3 md:grid-cols-4 gap-6">
        <div v-for="(skill, index) in skills" :key="index"
             class="p-6 bg-white dark:bg-gray-900 rounded-xl shadow-md hover:shadow-xl transition-all duration-300 group cursor-default"
             data-aos="zoom-in" :data-aos-delay="index * 50">

          <div class="flex justify-center mb-4 h-16 items-center">

            <div
               class="w-14 h-14 transition-transform duration-300 group-hover:scale-110 group-hover:-translate-y-1"
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

          </div>

          <h3 class="font-bold text-gray-700 dark:text-gray-200">{{ skill.name }}</h3>
        </div>
      </div>
    </div>
  </section>
</template>
