<script setup>
import { ref } from 'vue'

// Estado para controlar la visibilidad del contenido
const isMoreVisible = ref(false)

// Función para alternar la visibilidad
const toggleMore = () => {
  isMoreVisible.value = !isMoreVisible.value
}
</script>

<template>
  <div class="lg:hidden z-10 flex flex-col mt-10 md:mt-2">
    <h2 class="text-xl md:text-2xl font-semibold text-white">Muhammad Sultan Raisyah</h2>
    <h2 class="text-xl md:text-4xl font-semibold text-green-200">front-end developer</h2>
  </div>
  <div class="flex flex-col mt-4 md:mt-0">
    <div
      class="flex flex-col gap-4 p-2 md:text-start text-justify text-neutral-300 border border-green-200 md:rounded rounded-t-xl rounded-bl-xl glow-card"
    >
      <p class="tracking-wide leading-[1.6]">
        I'm a fresh graduate in Computer Science and a passionate front-end developer with
        internship experience at PetroChina International Jabung Ltd as an IT Support and Developer.
        During my time there, I was responsible for both troubleshooting IT-related issues and
        developing internal web applications.
      </p>
      <div
        id="more"
        :class="{ hidden: !isMoreVisible, 'md:flex': true, 'flex-col': true }"
        class="gap-4"
      >
        <p class="tracking-wide leading-[1.6]">
          My experience at PetroChina not only strengthened my problem-solving skills but also
          deepened my passion for building interactive user interfaces, where I found fulfillment in
          transforming complex ideas into seamless digital experiences through clean and efficient
          code. These are the techs that i like to use:
        </p>
        <div class="tracking-wide leading-[1.6] text-slate-300">
          <ul class="flex flex-wrap text-white list-disc list-inside">
            <li class="w-1/2">HTML</li>
            <li class="w-1/2">CSS</li>
            <li class="w-1/2">JavaScript</li>
            <li class="w-1/2">Tailwind CSS</li>
            <li class="w-1/2">Bootstrap</li>
            <li class="w-1/2">Vue.js</li>
            <li class="w-1/2">API Integration</li>
            <li class="w-1/2">Git</li>
          </ul>
        </div>
        <p class="tracking-wide leading-[1.6]">
          <span class="text-green-200">Think of it as a win-win: </span>you get a dedicated engineer
          eager to tackle challenges, and I get to grow while helping your company thrive. Let's
          connect and build something great together!
        </p>
      </div>
    </div>
    <div class="md:hidden w-full flex justify-end">
      <button
        @click="toggleMore"
        class="px-3 py-1 text-green-200 border-l border-r border-b border-green-200 rounded-bl rounded-br hover:bg-green-200/10"
      >
        {{ isMoreVisible ? 'read less..' : 'read more..' }}
      </button>
    </div>
  </div>
  <div
    class="hidden md:flex w-full justify-between md:justify-start mt-4 gap-2 md:gap-8 lg:gap-14 text-xs lg:text-[14px] relative"
  >
    <a
      href="/cv.pdf"
      target="_blank"
      rel="noopener noreferrer"
      class="px-4 py-3 border border-white text-white hover:text-gray-700 hover:bg-white transition-all rounded-2xl font-bold shadow-xl"
    >
      <i class="fa fa-file" aria-hidden="true"></i><span class="ml-2">Download CV</span>
    </a>
    <a
      href="https://mail.google.com/mail/?view=cm&fs=1&to=soeltaan@gmail.com"
      target="_blank"
      class="md:w-34 px-4 md:px-6 py-3 border border-white text-white rounded-2xl hover:text-gray-700 hover:bg-white transition-all duration-300 flex justify-center whitespace-nowrap shadow-xl"
    >
      <i class="fa fa-comments" aria-hidden="true"></i><span class="ml-2">Contact Me</span>
    </a>
  </div>
  <div
    class="flex md:hidden w-full justify-between mt-4 text-xs lg:text-[14px] relative border border-green-200 text-green-200 rounded-lg"
  >
    <a
      href="/cv.pdf"
      target="_blank"
      rel="noopener noreferrer"
      class="w-1/2 py-3 text-green-200 hover:text-gray-700 border-r border-green-200 hover:bg-white transition-all font-bold flex justify-center shadow-xl"
    >
      <i class="fa fa-file" aria-hidden="true"></i><span class="ml-2">Download CV</span>
    </a>

    <a
      href="https://mail.google.com/mail/?view=cm&fs=1&to=soeltaan@gmail.com"
      target="_blank"
      class="w-1/2 py-3 text-green-200 hover:text-gray-700 border-l border-green-200 hover:bg-white transition-all duration-300 flex justify-center whitespace-nowrap shadow-xl"
    >
      <i class="fa fa-comments" aria-hidden="true"></i><span class="ml-2">Contact Me</span>
    </a>
  </div>
</template>

<style scoped>
@media (min-width: 768px) {
  .glow-card::after {
    content: '';
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background: linear-gradient(315deg, #265844, #1c3947);
    filter: blur(8px);
    z-index: 0;
    border-radius: 0.75rem;
  }

  .glow-card > * {
    position: relative;
    z-index: 1;
  }
}
</style>
