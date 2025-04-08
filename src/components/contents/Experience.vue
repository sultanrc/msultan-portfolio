<script setup>
import petrochina from '@/assets/images/petrochina.png'
const skills = [
  'UI Design',
  'Figma',
  'Front-end Development',
  'HTML',
  'CSS',
  'PHP',
  'JavaScript',
  'CodeIgniter4',
  'Bootstrap',
]
</script>

<template>
  <h1 class="mb-2 text-white text-2xl">experience</h1>
  <a href="https://www.petrochina.co.id" target="_blank">
    <div class="p-4 rounded-lg group">
      <div class="flex flex-col">
        <h2 class="text-[12px] font-inter font-bold">FEBRUARY - JUNE 2023</h2>
        <div class="flex p-2">
          <div class="flex items-end">
            <img :src="petrochina" alt="PetroChina Logo" class="w-14 h-auto" />
          </div>
          <div class="w-3/4 md:w-full flex-row ms-4 text-sm font-semibold">
            <h2 class="text-xs xl:text-lg text-slate-300 my-1">IT Support and Developer</h2>
            <h2 class="text-xs xl:text-md text-slate-300">PetroChina International Jabung Ltd.</h2>
          </div>
        </div>
      </div>
      <p class="tracking-wide leading-[1.6] mt-2 md:pr-2 text-[12px]">
        I completed a six-month on-site internship at PetroChina International Jabung Ltd., based in
        Tanjung Jabung Timur, Jambi Province. The company is about an hour's drive from Jambi City
        and a one-hour flight from Jakarta, which is where I live. I worked at the IT Shop sector,
        wearing a company uniform, and followed a demanding schedule from 6 AM to 6 PM. Our main
        project was the Early Warning System, a web-based monitoring system for tracking server room
        temperatures. Additionally, I played a role as an IT Support technician, handling fiber
        optic cable maintenance and ensuring smooth network connectivity across the site.
      </p>
      <div class="flex flex-wrap gap-2 mt-4">
        <a
          v-for="(skill, index) in skills"
          :key="index"
          class="inline-block px-4 my-[1px] bg-slate-500 text-white rounded-2xl hover:bg-transparent hover:outline hover:outline-2 hover:outline-gray-700 transition-all"
        >
          <span class="text-[12px]">{{ skill }}</span>
        </a>
      </div>
    </div>
  </a>
  <div class="p-4 rounded-lg transition">more to come..</div>
</template>

<style scoped></style>
