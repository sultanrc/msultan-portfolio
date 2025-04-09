<script setup>
import { onMounted, defineEmits } from 'vue'
import About from './contents/About.vue'
import Experience from './contents/Experience.vue'
import Project from './contents/Project.vue'
import Footer from './contents/Footer.vue'

const emit = defineEmits(['scroll-update'])
const sections = ['about', 'experience', 'projects']

const handleScroll = () => {
  let currentSection = ''
  sections.forEach((section) => {
    const element = document.getElementById(section)
    if (element) {
      const rect = element.getBoundingClientRect()
      if (rect.top <= 100 && rect.bottom >= 100) {
        currentSection = section
      }
    }
  })

  emit('scroll-update', currentSection)
}
</script>
<template>
  <div
    @scroll="handleScroll"
    ref="scrollContainer"
    class="flex w-full flex-1 flex-col gap-12 md:gap-0 px-4 md:px-10 lg:px-16 max-h-screen pl-4 overflow-y-auto scrollbar-none"
  >
    <div
      id="about"
      class="flex flex-col items-center gap-2 px-6 md:mr-12 md:p-8 md:mt-20 md:scale-95 2xl:scale-100 2xl:mt-28 xl:text-sm text-xs md:outline md:outline-2 md:outline-neutral-600 rounded-xl shadow-xl"
    >
      <About />
    </div>

    <div id="experience" class="flex flex-col px-6 md:px-2 md:pt-20 md:mr-12 text-neutral-300">
      <Experience />
    </div>

    <div id="projects" class="flex flex-col md:pt-16 px-6 md:px-2 md:mr-12 text-neutral-300">
      <Project />
    </div>

    <Footer />
  </div>
</template>

<style scoped></style>
