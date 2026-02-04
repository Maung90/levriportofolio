<script setup>
const projects = [

  {
    title: 'Senang Tours & Travel',
    desc: 'Sistem informasi pariwisata terintegrasi yang mencakup autentikasi multi-user aman dan manajemen paket wisata berbasis CodeIgniter 3 dan sekarang telah di upgrade menjadi laravel 11',
    img: '/images/project/login2.PNG',
    tags: ['PHP', 'CI3', 'Bootstrap', 'Laravel'],
    link: 'https://github.com/Maung90/ReservasiTour/',
    color: 'bg-blue-500'
  },
  {
    title: 'Dashboard PinjamBarang',
    desc: 'Aplikasi manajemen inventaris aset dengan dashboard monitoring real-time untuk mempermudah pelacakan sirkulasi barang masuk dan keluar.',
    img: '/images/project/dashboard.PNG',
    tags: ['CodeIgniter', 'MySQL'],
    link: 'https://github.com/Maung90/PinjamBarang/',
    color: 'bg-red-500'
  },
  {
    title: 'MyChat App',
    desc: 'Aplikasi pesan instan mobile (Real-time Chat) dengan performa tinggi dan antarmuka modern yang dikembangkan menggunakan ekosistem Flutter.',
    img: '/images/project/flutter.png',
    tags: ['Flutter', 'Dart'],
    link: 'https://github.com/Maung90/mychat/',
    color: 'bg-blue-400'
  },
  {
    title: 'Dengerin',
    desc: 'Platform streaming musik responsif dengan fitur pemutar audio interaktif dan manajemen playlist, dibangun dengan struktur PHP Native yang efisien.',
    img: '/images/project/dengerin.png',
    tags: ['PHP', 'Bootstrap'],
    link: 'https://github.com/Maung90/dengerin/',
    color: 'bg-purple-500'
  }
];
</script>

<template>
  <section id="project" class="py-20 bg-gray-50 dark:bg-gray-800 transition-colors">
    <div class="max-w-5xl mx-auto px-4 sm:px-6 lg:px-8">

      <div class="text-center mb-12" data-aos="fade-up">
        <h2 class="text-3xl font-bold mb-4 text-gray-900 dark:text-white">Gallery Projects</h2>
        <p class="text-gray-500 dark:text-gray-400">Berikut adalah project yang pernah saya kerjakan</p>
      </div>

      <div class="grid grid-cols-2 md:grid-cols-2 gap-8">
        <div v-for="(project, index) in projects" :key="index"
             class="bg-white dark:bg-gray-900 rounded-2xl shadow-lg overflow-hidden hover:shadow-2xl transition-all duration-300 transform hover:-translate-y-2 group border border-gray-100 dark:border-gray-700"
             data-aos="zoom-in" :data-aos-delay="index * 100">

          <div class="relative overflow-hidden h-56"> <img :src="project.img" :alt="project.title" class="w-full h-full object-cover transition-transform duration-500 group-hover:scale-110">

            <div class="absolute inset-0 bg-black/60 opacity-0 group-hover:opacity-100 transition-opacity duration-300 flex items-center justify-center backdrop-blur-sm">
              <a :href="project.link" target="_blank" class="text-white border border-white px-6 py-2 rounded-full hover:bg-white hover:text-black transition font-medium">
                View Project
              </a>
            </div>
          </div>

          <div class="p-6">
            <h3 class="text-xl font-bold mb-2 flex justify-between items-center text-gray-900 dark:text-white">
              {{ project.title }}
              <a :href="project.link" target="_blank" class="text-gray-400 hover:text-primary transition-colors">
                <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="w-5 h-5">
                  <path stroke-linecap="round" stroke-linejoin="round" d="M13.5 6H5.25A2.25 2.25 0 0 0 3 8.25v10.5A2.25 2.25 0 0 0 5.25 21h10.5A2.25 2.25 0 0 0 18 18.75V10.5m-10.5 6L21 3m0 0h-5.25M21 3v5.25" />
                </svg>
              </a>
            </h3>
            <p class="text-gray-600 dark:text-gray-400 text-sm mb-4 min-h-[50px] leading-relaxed">{{ project.desc }}</p>
            <div class="flex flex-wrap gap-2">
              <span v-for="tag in project.tags" :key="tag"
                    class="px-3 py-1 text-xs font-semibold text-white rounded-full bg-primary shadow-sm">
                {{ tag }}
              </span>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>
