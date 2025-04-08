<script setup>
import { ref, onMounted } from 'vue'

const buttonText = ref('Contact Me')

const handleMouseEnter = () => {
  buttonText.value = 'Hit Me Up!'
}

const handleMouseLeave = () => {
  buttonText.value = 'Contact Me'
}
</script>

<template>
  <div class="md:hidden flex flex-col pt-16 pb-8">
    <h2 class="text-xl md:text-2xl font-semibold text-white">Muhammad Sultan Raisyah</h2>
    <h2 class="text-xl md:text-4xl font-semibold text-white">front-end developer</h2>
    <h2 class="text-lg md:text-xl font-inter font-semibold text-green-200">
      Computer Science Fresh Graduate
    </h2>
  </div>
  <div class="flex flex-col gap-4">
    <p class="tracking-wide leading-[1.6]">
      I’m a fresh graduate in Computer Science and a passionate front-end developer with internship
      experience at PetroChina International Jabung Ltd as an IT Support and Developer. During my
      time there, I was responsible for both troubleshooting IT-related issues and developing
      internal web applications.
    </p>
    <p class="tracking-wide leading-[1.6]">
      My experience at PetroChina not only strengthened my problem-solving skills but also deepened
      my passion for building interactive user interfaces. I enjoy crafting seamless digital
      experiences—though, let’s be real, <span class="text-green-200">Vue.js</span> is my current
      go-to.
    </p>
    <p class="tracking-wide leading-[1.6] text-slate-300">
      One of my notable projects, showcased in the
      <a href="#projects" class="text-green-200">Projects</a> section, reflects my ability to create
      efficient and user-friendly applications. I’m now looking for opportunities in Front-End
      Development where I can apply my skills while contributing to impactful projects. I'm also
      open to internship opportunities to further refine my expertise in real-world scenarios.
    </p>
    <p class="tracking-wide leading-[1.6] text-slate-300">
      <span class="text-green-200">Think of it as a win-win: </span>you get a dedicated engineer
      eager to tackle challenges, and I get to grow while helping your company thrive. Let’s connect
      and build something great together!
    </p>
  </div>
  <div
    class="flex w-full justify-between md:justify-start mt-4 gap-2 md:gap-8 lg:gap-14 text-xs lg:text-[14px] relative"
  >
    <a
      href="/cv.pdf"
      target="_blank"
      rel="noopener noreferrer"
      class="px-4 py-3 text-gray-700 bg-white border-white hover:bg-transparent hover:text-white hover:outline hover:outline-1 hover:outline-outline-gray-700 transition-all rounded-2xl font-bold"
    >
      <i class="fa fa-file" aria-hidden="true"></i><span class="ml-2">Download CV</span>
    </a>
    <a
      href="https://mail.google.com/mail/?view=cm&fs=1&to=soeltaan@gmail.com"
      target="_blank"
      class="md:w-34 px-4 md:px-6 py-3 border border-white text-white rounded-2xl hover:text-gray-700 hover:bg-white transition-all duration-300 flex justify-center whitespace-nowrap"
      @mouseenter="handleMouseEnter"
      @mouseleave="handleMouseLeave"
    >
      <i class="fa fa-comments" aria-hidden="true"></i><span class="ml-2">{{ buttonText }}</span>
    </a>
  </div>
</template>

<style scoped></style>
