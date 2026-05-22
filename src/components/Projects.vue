<script setup>
const projects = [
  {
    title: 'Sistem Deteksi URL Phishing',
    desc: 'Aplikasi keamanan siber berbasis machine learning yang menganalisis dan mengklasifikasi URL secara real-time untuk mendeteksi ancaman phishing, didukung REST API FastAPI dan antarmuka Vue yang responsif.',
    img: '/images/project/deteksi-phishing.png',
    tags: ['Vue', 'Tailwind', 'FastAPI', 'Python'],
    link: 'https://github.com/Maung90/phishing-detector-vue',
    num: '01',
    isPrivate: false
  },
  {
    title: 'Sistem Rapat',
    desc: 'Aplikasi manajemen rapat lintas platform yang mendukung penjadwalan dan dokumentasi notulensi secara terpusat, dibangun dengan Flutter untuk mobile dan Laravel sebagai backend API.',
    img: '/images/project/sistem-rapat.png',
    tags: ['Flutter', 'Laravel', 'PHP'],
    link: 'https://github.com/Maung90/ReservasiTour/',
    num: '02',
    isPrivate: true
  },
  {
    title: 'Senang Tours & Travel',
    desc: 'Sistem reservasi wisata terintegrasi dengan manajemen paket tour, autentikasi multi-role, dan dashboard admin. Dibangun awal dengan CodeIgniter 3 lalu dimigrasi ke Laravel 11 untuk skalabilitas lebih baik.',
    img: '/images/project/login2.PNG',
    tags: ['PHP', 'CI3', 'Bootstrap', 'Laravel'],
    link: 'https://github.com/Maung90/ReservasiTour/',
    num: '03',
    isPrivate: false
  },
  {
    title: 'Dashboard PinjamBarang',
    desc: 'Sistem manajemen inventaris aset instansi dengan dashboard monitoring real-time, pelacakan sirkulasi barang masuk dan keluar, serta laporan peminjaman berbasis peran pengguna.',
    img: '/images/project/dashboard.PNG',
    tags: ['CodeIgniter', 'MySQL'],
    link: 'https://github.com/Maung90/PinjamBarang/',
    num: '04',
    isPrivate: false
  },
  {
    title: 'MyChat App',
    desc: 'Aplikasi pesan instan mobile berbasis Flutter dengan fitur real-time messaging, manajemen kontak, dan antarmuka modern yang ringan dan responsif di berbagai ukuran layar.',
    img: '/images/project/flutter.png',
    tags: ['Flutter', 'Dart'],
    link: 'https://github.com/Maung90/mychat/',
    num: '05',
    isPrivate: false
  },
  {
    title: 'Dengerin',
    desc: 'Platform streaming musik dengan pemutar audio interaktif, manajemen playlist, dan pencarian lagu. Dibangun menggunakan PHP Native dengan arsitektur MVC sederhana yang efisien.',
    img: '/images/project/dengerin.png',
    tags: ['PHP', 'Bootstrap'],
    link: 'https://github.com/Maung90/dengerin/',
    num: '06',
    isPrivate: false
  }
];
</script>

<template>
  <section id="project" class="py-20 sm:py-28 px-5 sm:px-8 bg-gray-50 dark:bg-gray-950 transition-colors">
    <div class="max-w-6xl mx-auto">

      <!-- Section header -->
      <div class="flex flex-col sm:flex-row sm:items-end justify-between mb-12 sm:mb-16 gap-4" data-aos="fade-up">
        <div>
          <span class="text-xs font-semibold tracking-[0.2em] uppercase text-gray-400 dark:text-gray-500">Portfolio</span>
          <h2 class="text-4xl sm:text-5xl font-black tracking-tighter text-gray-900 dark:text-white mt-2">
            Selected<br>Projects
          </h2>
        </div>
        <p class="text-gray-400 dark:text-gray-500 text-sm max-w-xs sm:text-right">
          Project yang pernah saya kerjakan selama belajar & magang.
        </p>
      </div>

      <!-- Project list -->
      <div class="flex flex-col gap-3 border border-gray-200 dark:border-gray-800">
        <div
          v-for="(project, index) in projects"
          :key="index"
          class="group relative bg-white dark:bg-black overflow-hidden"
          data-aos="fade-up"
          :data-aos-delay="index * 80"
        >
          <!-- Mobile: stacked card -->
          <!-- Desktop: horizontal row (image left, info right) -->
          <div class="flex flex-col lg:flex-row">

            <!-- Image -->
            <div class="relative lg:w-3/5 shrink-0 overflow-hidden bg-gray-100 dark:bg-gray-900">
              <!-- aspect-ratio 2:1 for mobile, fixed height for desktop -->
              <div class="aspect-[2/1] lg:aspect-auto lg:h-full min-h-[14rem]">
                <img
                  :src="project.img"
                  :alt="project.title"
                  class="w-full h-full object-cover object-top transition-transform duration-700 group-hover:scale-[1.03]"
                >
              </div>

              <!-- Hover overlay (desktop only) -->
              <div class="absolute inset-0 bg-black/60 opacity-0 group-hover:opacity-100 transition-opacity duration-300 hidden lg:flex items-center justify-center">
                <span v-if="project.isPrivate" class="inline-flex items-center gap-2 text-white/70 text-sm font-bold tracking-widest uppercase border border-white/30 px-5 py-2.5 cursor-default select-none">
                  <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="2" stroke="currentColor" class="w-3.5 h-3.5">
                    <path stroke-linecap="round" stroke-linejoin="round" d="M16.5 10.5V6.75a4.5 4.5 0 1 0-9 0v3.75m-.75 11.25h10.5a2.25 2.25 0 0 0 2.25-2.25v-6.75a2.25 2.25 0 0 0-2.25-2.25H6.75a2.25 2.25 0 0 0-2.25 2.25v6.75a2.25 2.25 0 0 0 2.25 2.25Z" />
                  </svg>
                  Private Repo
                </span>
                <a v-else :href="project.link" target="_blank" class="flex items-center gap-2 text-white text-sm font-bold tracking-widest uppercase border border-white px-5 py-2.5 hover:bg-white hover:text-black transition-colors duration-200">
                  View Project
                  <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="2" stroke="currentColor" class="w-3.5 h-3.5">
                    <path stroke-linecap="round" stroke-linejoin="round" d="m4.5 19.5 15-15m0 0H8.25m11.25 0v11.25" />
                  </svg>
                </a>
              </div>
            </div>

            <!-- Info panel -->
            <div class="flex flex-col justify-between p-5 sm:p-6 lg:p-8 lg:w-2/5">
              <div>
                <!-- Number + title row -->
                <div class="flex items-start justify-between gap-3 mb-3">
                  <div>
                    <span class="text-xs font-bold tracking-widest text-gray-300 dark:text-gray-700 block mb-1">{{ project.num }}</span>
                    <h3 class="font-bold text-lg sm:text-xl text-gray-900 dark:text-white leading-tight">
                      {{ project.title }}
                    </h3>
                  </div>
                  <a v-if="!project.isPrivate" :href="project.link" target="_blank" class="shrink-0 text-gray-300 dark:text-gray-700 hover:text-gray-900 dark:hover:text-white transition-colors mt-1">
                    <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="w-5 h-5">
                      <path stroke-linecap="round" stroke-linejoin="round" d="m4.5 19.5 15-15m0 0H8.25m11.25 0v11.25" />
                    </svg>
                  </a>
                  <span v-else class="shrink-0 text-gray-300 dark:text-gray-700 mt-1" title="Private Repo">
                    <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="w-5 h-5">
                      <path stroke-linecap="round" stroke-linejoin="round" d="M16.5 10.5V6.75a4.5 4.5 0 1 0-9 0v3.75m-.75 11.25h10.5a2.25 2.25 0 0 0 2.25-2.25v-6.75a2.25 2.25 0 0 0-2.25-2.25H6.75a2.25 2.25 0 0 0-2.25 2.25v6.75a2.25 2.25 0 0 0 2.25 2.25Z" />
                    </svg>
                  </span>
                </div>

                <p class="text-gray-500 dark:text-gray-400 text-sm leading-relaxed mb-5">{{ project.desc }}</p>
              </div>

              <!-- Tags + mobile CTA -->
              <div class="flex flex-col gap-4">
                <div class="flex flex-wrap gap-1.5">
                  <span
                    v-for="tag in project.tags"
                    :key="tag"
                    class="px-2.5 py-0.5 text-xs font-semibold bg-gray-100 dark:bg-gray-900 text-gray-600 dark:text-gray-400 border border-gray-200 dark:border-gray-800"
                  >
                    {{ tag }}
                  </span>
                </div>

                <!-- CTA visible on mobile -->
                <span v-if="project.isPrivate" class="lg:hidden inline-flex items-center gap-2 text-sm font-semibold text-gray-400 dark:text-gray-600 cursor-default select-none">
                  <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="2" stroke="currentColor" class="w-3.5 h-3.5">
                    <path stroke-linecap="round" stroke-linejoin="round" d="M16.5 10.5V6.75a4.5 4.5 0 1 0-9 0v3.75m-.75 11.25h10.5a2.25 2.25 0 0 0 2.25-2.25v-6.75a2.25 2.25 0 0 0-2.25-2.25H6.75a2.25 2.25 0 0 0-2.25 2.25v6.75a2.25 2.25 0 0 0 2.25 2.25Z" />
                  </svg>
                  Private Repo
                </span>
                <a v-else :href="project.link" target="_blank" class="lg:hidden inline-flex items-center gap-2 text-sm font-bold text-gray-900 dark:text-white underline underline-offset-4 hover:opacity-60 transition-opacity">
                  View Project
                  <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="2" stroke="currentColor" class="w-3.5 h-3.5">
                    <path stroke-linecap="round" stroke-linejoin="round" d="m4.5 19.5 15-15m0 0H8.25m11.25 0v11.25" />
                  </svg>
                </a>
              </div>
            </div>

          </div>
        </div>
      </div>

    </div>
  </section>
</template>
