<script setup>
const experiences = [
  {
    year: 'Juli – Desember 2025',
    role: 'Software Engineer Intern',
    company: 'Diskominfo Command Center Badung',
    desc: [
      'Mendesain antarmuka (UI/UX) aplikasi mobile layanan publik yang intuitif dan berfokus pada kemudahan akses pengguna.',
      'Merancang arsitektur database yang efisien dan ternormalisasi untuk mendukung kinerja aplikasi yang optimal.',
      'Mengembangkan RESTful API yang aman dan scalable menggunakan framework Laravel sebagai fondasi integrasi sistem.'
    ]
  },
  {
    year: 'Maret – April 2021',
    role: 'Research & Development Intern',
    company: 'Bisma Informatika',
    desc: [
      'Membangun sistem informasi perpustakaan digital untuk mendigitalisasi proses sirkulasi peminjaman buku.',
      'Mengimplementasikan desain web responsif agar aplikasi dapat diakses optimal di berbagai perangkat.',
      'Merancang struktur database manajemen aset buku dan data anggota untuk memastikan validitas data.'
    ]
  }
];

const educations = [
  {
    year: 'Sep 2022 – Sekarang',
    school: 'Politeknik Negeri Bali',
    major: 'Teknologi Informasi',
    status: 'Active'
  },
  {
    year: 'Juli 2019 – Juni 2022',
    school: 'SMK TI Bali Global Denpasar',
    major: 'Rekayasa Perangkat Lunak',
    status: null
  }
];
</script>

<template>
  <section id="resume" class="py-20 sm:py-28 px-5 sm:px-8 bg-white dark:bg-black transition-colors">
    <div class="max-w-6xl mx-auto">

      <!-- Section header -->
      <div class="mb-12 sm:mb-16" data-aos="fade-up">
        <span class="text-xs font-semibold tracking-[0.2em] uppercase text-gray-400 dark:text-gray-500">Background</span>
        <h2 class="text-4xl sm:text-5xl font-black tracking-tighter text-gray-900 dark:text-white mt-2">
          Resume
        </h2>
      </div>

      <div class="grid grid-cols-1 lg:grid-cols-2 gap-12 lg:gap-16">

        <!-- Experience -->
        <div data-aos="fade-right">
          <h3 class="text-xs font-bold tracking-[0.2em] uppercase text-gray-400 dark:text-gray-500 mb-8 flex items-center gap-3">
            <span class="w-6 h-px bg-gray-300 dark:bg-gray-700"></span>
            Experience
          </h3>

          <div class="space-y-8">
            <div
              v-for="(exp, index) in experiences"
              :key="index"
              class="group relative pl-5 border-l border-gray-200 dark:border-gray-800 hover:border-gray-900 dark:hover:border-gray-400 transition-colors duration-300"
            >
              <!-- Dot -->
              <div class="absolute -left-[5px] top-1 w-2.5 h-2.5 rounded-full bg-white dark:bg-black border-2 border-gray-300 dark:border-gray-700 group-hover:border-gray-900 dark:group-hover:border-gray-400 transition-colors duration-300"></div>

              <span class="text-xs text-gray-400 dark:text-gray-500 font-mono">{{ exp.year }}</span>
              <h4 class="font-bold text-gray-900 dark:text-white mt-1 text-base sm:text-lg">{{ exp.role }}</h4>
              <p class="text-sm text-gray-400 dark:text-gray-500 font-medium mb-3">{{ exp.company }}</p>
              <ul class="space-y-1.5">
                <li
                  v-for="(point, i) in exp.desc"
                  :key="i"
                  class="text-sm text-gray-500 dark:text-gray-400 leading-relaxed flex gap-2"
                >
                  <span class="shrink-0 text-gray-300 dark:text-gray-700 mt-1">—</span>
                  {{ point }}
                </li>
              </ul>
            </div>
          </div>
        </div>

        <!-- Education -->
        <div data-aos="fade-left">
          <h3 class="text-xs font-bold tracking-[0.2em] uppercase text-gray-400 dark:text-gray-500 mb-8 flex items-center gap-3">
            <span class="w-6 h-px bg-gray-300 dark:bg-gray-700"></span>
            Education
          </h3>

          <div class="space-y-8">
            <div
              v-for="(edu, index) in educations"
              :key="index"
              class="group relative pl-5 border-l border-gray-200 dark:border-gray-800 hover:border-gray-900 dark:hover:border-gray-400 transition-colors duration-300"
            >
              <!-- Dot -->
              <div class="absolute -left-[5px] top-1 w-2.5 h-2.5 rounded-full bg-white dark:bg-black border-2 border-gray-300 dark:border-gray-700 group-hover:border-gray-900 dark:group-hover:border-gray-400 transition-colors duration-300"></div>

              <div class="flex items-center gap-2">
                <span class="text-xs text-gray-400 dark:text-gray-500 font-mono">{{ edu.year }}</span>
                <span
                  v-if="edu.status"
                  class="text-xs bg-gray-900 dark:bg-white text-white dark:text-black px-2 py-0.5 font-bold tracking-wide"
                >
                  {{ edu.status }}
                </span>
              </div>
              <h4 class="font-bold text-gray-900 dark:text-white mt-1 text-base sm:text-lg">{{ edu.school }}</h4>
              <p class="text-sm text-gray-400 dark:text-gray-500 font-medium uppercase tracking-wide mt-0.5">{{ edu.major }}</p>
            </div>
          </div>
        </div>

      </div>
    </div>
  </section>
</template>
