<script setup>
import { computed } from 'vue'
import porto from '@/assets/images/porto.jpeg'
import ews from '@/assets/images/ews.jpeg'

const experienceContainer = computed(
  () =>
    'flex flex-col p-4 rounded-lg transition hover:bg-gray-700 hover:bg-opacity-10  hover:shadow-xl group',
)
</script>

<template>
  <h1 class="mb-4 text-white text-2xl leading-[1.6]">projects</h1>
  <div :class="experienceContainer">
    <div class="flex flex-col lg:flex-row gap-4">
      <div>
        <img
          :src="ews"
          class="md:w-[1440px] h-24 rounded-lg border border-gray-400 group-hover:scale-105 transition group-hover:-translate-x-1"
          alt="Portfolio Image"
        />
      </div>
      <div class="flex flex-col ms-2">
        <h2 class="text-m font-inter font-bold text-slate-300 flex items-center">
          Early Warning System
          <svg
            xmlns="http://www.w3.org/2000/svg"
            viewBox="0 0 512 512"
            class="w-4 h-4 ml-2 text-slate-600 fill-current group-hover:-translate-y-1 group-hover:text-white transition"
          >
            <path
              d="M320 0c-17.7 0-32 14.3-32 32s14.3 32 32 32l82.7 0L201.4 265.4c-12.5 12.5-12.5 32.8 0 45.3s32.8 12.5 45.3 0L448 109.3l0 82.7c0 17.7 14.3 32 32 32s32-14.3 32-32l0-160c0-17.7-14.3-32-32-32L320 0zM80 32C35.8 32 0 67.8 0 112L0 432c0 44.2 35.8 80 80 80l320 0c44.2 0 80-35.8 80-80l0-112c0-17.7-14.3-32-32-32s-32 14.3-32 32l0 112c0 8.8-7.2 16-16 16L80 448c-8.8 0-16-7.2-16-16l0-320c0-8.8 7.2-16 16-16l112 0c17.7 0 32-14.3 32-32s-14.3-32-32-32L80 32z"
            />
          </svg>
        </h2>
        <p class="tracking-wide leading-[1.4] mt-2 text-xs group-hover:text-white">
          The Early Warning System (EWS) monitors server room conditions using an ESP8266 and a
          DHT11 sensor, which measures temperature and humidity in real-time. Data is sent to a
          database and displayed on a web dashboard for easy monitoring. I contributed by designing
          the UI, slicing it into HTML, CSS, and Bootstrap, and adding interactivity with
          JavaScript. Developed in CodeIgniter 4, the system triggers alerts if the temperature
          exceeds 30°C or humidity surpasses 80%, helping IT staff prevent overheating.
        </p>
      </div>
    </div>
  </div>
  <div :class="experienceContainer">
    <div class="flex flex-col lg:flex-row gap-4">
      <div>
        <img
          :src="porto"
          class="md:w-[1440px] h-24 rounded-lg border border-gray-400 group-hover:scale-105 transition group-hover:-translate-x-1"
          alt="Portfolio Image"
        />
      </div>
      <div class="flex flex-col ms-2">
        <h2 class="text-m font-inter font-bold text-slate-300 flex items-center">
          Vue based Portofolio
          <svg
            xmlns="http://www.w3.org/2000/svg"
            viewBox="0 0 512 512"
            class="w-4 h-4 ml-2 text-slate-600 fill-current group-hover:-translate-y-1 group-hover:text-white transition"
          >
            <path
              d="M320 0c-17.7 0-32 14.3-32 32s14.3 32 32 32l82.7 0L201.4 265.4c-12.5 12.5-12.5 32.8 0 45.3s32.8 12.5 45.3 0L448 109.3l0 82.7c0 17.7 14.3 32 32 32s32-14.3 32-32l0-160c0-17.7-14.3-32-32-32L320 0zM80 32C35.8 32 0 67.8 0 112L0 432c0 44.2 35.8 80 80 80l320 0c44.2 0 80-35.8 80-80l0-112c0-17.7-14.3-32-32-32s-32 14.3-32 32l0 112c0 8.8-7.2 16-16 16L80 448c-8.8 0-16-7.2-16-16l0-320c0-8.8 7.2-16 16-16l112 0c17.7 0 32-14.3 32-32s-14.3-32-32-32L80 32z"
            />
          </svg>
        </h2>
        <p class="tracking-wide leading-[1.4] mt-2 text-xs group-hover:text-white">
          I built my own portfolio website using Vue and Tailwind, because, you know, every
          developer needs a fancy place to flex their skills. The site has an About, Experience, and
          a Projects section showcasing my work. And since I was running low on projects, I
          shamelessly added this very portfolio site to the Projects section—because why not? 😁
          It’s a fun little project where I experimented with clean UI, smooth animations, and just
          enough personality to make recruiters smile (hopefully).
        </p>
      </div>
    </div>
  </div>

  <div class="p-4 rounded-lg transition">more to come..</div>
</template>

<style scoped></style>
