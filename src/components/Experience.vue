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
    ],
    color: 'bg-blue-500'
  },
  {
    year: 'Maret – April 2021',
    role: 'Research & Development Intern',
    company: 'Bisma Informatika',
    desc: [
      'Membangun sistem informasi perpustakaan digital untuk mendigitalisasi proses sirkulasi peminjaman buku.',
      'Mengimplementasikan desain web responsif (responsive layout) agar aplikasi dapat diakses optimal di berbagai perangkat.',
      'Merancang struktur database manajemen aset buku dan data anggota untuk memastikan validitas data.'
    ],
    color: 'bg-primary'
  }
];

const educations = [
  {
    year: 'Sep 2022 - Sekarang',
    school: 'Politeknik Negeri Bali',
    major: 'Teknologi Informasi',
    color: 'bg-green-500'
  },
  {
    year: 'Juli 2019 – Juni 2022',
    school: 'SMK TI Bali Global Denpasar',
    major: 'Rekayasa Perangkat Lunak',
    color: 'bg-gray-400'
  }
];
</script>

<template>
  <section id="resume" class="py-20 px-4 bg-white dark:bg-gray-900 transition-colors">
    <div class="max-w-7xl mx-auto grid grid-cols-2 md:grid-cols-2 gap-12">

      <div data-aos="fade-right">
        <h2 class="text-3xl font-bold mb-8 border-b-4 border-primary inline-block pb-2 text-gray-900 dark:text-white">Experience</h2>
        <div class="relative border-l-4 border-gray-200 dark:border-gray-700 ml-3 space-y-10">

          <div v-for="(exp, index) in experiences" :key="index" class="mb-10 ml-6 group">
            <span class="absolute -left-3 flex items-center justify-center w-6 h-6 rounded-full ring-4 ring-white dark:ring-gray-900 transition-transform group-hover:scale-110"
                  :class="exp.color">
            </span>

            <span class="block mb-1 text-sm font-normal leading-none text-gray-500 dark:text-gray-400">
              {{ exp.year }}
            </span>

            <h3 class="flex flex-col sm:flex-row sm:items-center mb-1 text-lg font-bold text-gray-900 dark:text-white">
              {{ exp.role }}
              <span class="hidden sm:block mx-2 text-gray-400">|</span>
              <span class="text-sm font-medium text-primary mt-1 sm:mt-0">{{ exp.company }}</span>
            </h3>

            <ul class="mb-4 text-base font-normal text-gray-600 dark:text-gray-300 list-disc ml-4 space-y-1">
              <li v-for="(point, i) in exp.desc" :key="i">
                {{ point }}
              </li>
            </ul>
          </div>

        </div>
      </div>

      <div data-aos="fade-left">
        <h2 class="text-3xl font-bold mb-8 border-b-4 border-primary inline-block pb-2 text-gray-900 dark:text-white">Education</h2>
        <div class="relative border-l-4 border-gray-200 dark:border-gray-700 ml-3 space-y-10">

          <div v-for="(edu, index) in educations" :key="index" class="mb-10 ml-6 group">
            <span class="absolute -left-3 flex items-center justify-center w-6 h-6 rounded-full ring-4 ring-white dark:ring-gray-900 transition-transform group-hover:scale-110"
                  :class="edu.color">
            </span>

            <span class="block mb-1 text-sm font-normal leading-none text-gray-500 dark:text-gray-400">
              {{ edu.year }}
            </span>

            <h3 class="text-lg font-bold text-gray-900 dark:text-white mt-1">
              {{ edu.school }}
            </h3>

            <p class="text-base font-medium text-gray-600 dark:text-gray-300 uppercase tracking-wide mt-1">
              {{ edu.major }}
            </p>
          </div>

        </div>
      </div>

    </div>
  </section>
</template>
