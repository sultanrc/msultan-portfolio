<script setup>
import { ref, onMounted, defineProps, defineEmits } from 'vue'

const props = defineProps(['activeTab'])
const emit = defineEmits(['tab-click'])

const sections = ['about', 'experience', 'projects']

const fullText = 'Transforming ideas into stunning visuals and seamless digital experiences.'
const displayedText = ref('')
let index = 0

const typeEffect = () => {
  if (index < fullText.length) {
    displayedText.value += fullText[index]
    index++
    setTimeout(typeEffect, 50) // Kecepatan mengetik (50ms per karakter)
  }
}

onMounted(() => {
  typeEffect()
})
</script>

<template>
  <div
    class="flex flex-1 flex-col gap-24 pl-10 pr-10 lg:pl-20 2xl:pr-56 md:py-24 2xl:py-28 md:mx-20 2xl:mx-0 fixed-col"
  >
    <div
      class="justify-center 2xl:mt-4 p-6 lg:h-[200px] flex flex-col gap-2 outline outline-2 outline-neutral-600 rounded-xl scale-90 2xl:scale-100 glow-card"
    >
      <h2 class="text-xl lg:text-4xl font-inter font-bold text-white">Muhammad Sultan</h2>
      <h2 class="text-3xl lg:text-xl font-semibold text-green-200">front-end developer</h2>
      <p class="text-md pr-18 leading-[1.6] text-slate-300">
        {{ displayedText }}
      </p>
    </div>
    <div
      class="hidden ml-6 md:flex flex-col items-start text-slate-400 text-xl"
      style="transform: perspective(800px) rotateY(10deg)"
    >
      <button
        v-for="section in sections"
        :key="section"
        @click="emit('tab-click', section)"
        :class="{
          'hover:text-white hover:text-3xl transition-all': true, // Class statis
          'text-white text-3xl transition-all': props.activeTab === section,
          'text-gray-500': props.activeTab !== section,
        }"
      >
        <span v-if="props.activeTab === section" class="arrow">▶</span>
        {{ section }}
      </button>
    </div>
    <div class="absolute bottom-24 left-30 flex gap-6 transform -skew-y-10">
      <a
        href="https://www.instagram.com/sultanr31/"
        class="group"
        target="_blank"
        rel="noopener noreferrer"
      >
        <svg
          xmlns="http://www.w3.org/2000/svg"
          width="34"
          height="34"
          viewBox="0 0 24 24"
          fill="none"
          stroke="currentColor"
          stroke-width="2"
          stroke-linecap="round"
          stroke-linejoin="round"
          class="lucide lucide-instagram text-slate-400 hover:scale-150 transition hover:animate-pulse hover:text-white hover:rotate-[10deg]"
        >
          <rect width="20" height="20" x="2" y="2" rx="5" ry="5" />
          <path d="M16 11.37A4 4 0 1 1 12.63 8 4 4 0 0 1 16 11.37z" />
          <line x1="17.5" x2="17.51" y1="6.5" y2="6.5" />
        </svg>
      </a>
      <a href="https://github.com/sultanrc" target="_blank" rel="noopener noreferrer">
        <svg
          width="34"
          height="34"
          viewBox="0 0 20 20"
          version="1.1"
          xmlns="http://www.w3.org/2000/svg"
          xmlns:xlink="http://www.w3.org/1999/xlink"
          class="hover:scale-150 transition hover:text-white hover:animate-pulse text-slate-400"
        >
          <g id="Page-1" stroke="none" stroke-width="1" fill="none" fill-rule="evenodd">
            <g
              id="Dribbble-Light-Preview"
              transform="translate(-140.000000, -7559.000000)"
              fill="currentColor"
            >
              <g id="icons" transform="translate(56.000000, 160.000000)">
                <path
                  d="M94,7399 C99.523,7399 104,7403.59 104,7409.253 C104,7413.782 101.138,7417.624 97.167,7418.981 C96.66,7419.082 96.48,7418.762 96.48,7418.489 C96.48,7418.151 96.492,7417.047 96.492,7415.675 C96.492,7414.719 96.172,7414.095 95.813,7413.777 C98.04,7413.523 100.38,7412.656 100.38,7408.718 C100.38,7407.598 99.992,7406.684 99.35,7405.966 C99.454,7405.707 99.797,7404.664 99.252,7403.252 C99.252,7403.252 98.414,7402.977 96.505,7404.303 C95.706,7404.076 94.85,7403.962 94,7403.958 C93.15,7403.962 92.295,7404.076 91.497,7404.303 C89.586,7402.977 88.746,7403.252 88.746,7403.252 C88.203,7404.664 88.546,7405.707 88.649,7405.966 C88.01,7406.684 87.619,7407.598 87.619,7408.718 C87.619,7412.646 89.954,7413.526 92.175,7413.785 C91.889,7414.041 91.63,7414.493 91.54,7415.156 C90.97,7415.418 89.522,7415.871 88.63,7414.304 C88.63,7414.304 88.101,7413.319 87.097,7413.247 C87.097,7413.247 86.122,7413.234 87.029,7413.87 C87.029,7413.87 87.684,7414.185 88.139,7415.37 C88.139,7415.37 88.726,7417.2 91.508,7416.58 C91.513,7417.437 91.522,7418.245 91.522,7418.489 C91.522,7418.76 91.338,7419.077 90.839,7418.982 C86.865,7417.627 84,7413.783 84,7409.253 C84,7403.59 88.478,7399 94,7399"
                  id="github-[#142]"
                ></path>
              </g>
            </g>
          </g>
        </svg>
      </a>
      <a href="https://www.linkedin.com/in/msultanr3152/" target="_blank" rel="noopener noreferrer">
        <svg
          fill="currentColor"
          width="34"
          height="34"
          viewBox="0 0 32 32"
          xmlns="http://www.w3.org/2000/svg"
          class="hover:scale-150 transition hover:text-white hover:-rotate-[5deg] hover:animate-pulse text-slate-400"
        >
          <path
            d="M27.26 27.271h-4.733v-7.427c0-1.771-0.037-4.047-2.475-4.047-2.468 0-2.844 1.921-2.844 3.916v7.557h-4.739v-15.271h4.552v2.083h0.061c0.636-1.203 2.183-2.468 4.491-2.468 4.801 0 5.692 3.161 5.692 7.271v8.385zM7.115 9.912c-1.527 0-2.751-1.235-2.751-2.756 0-1.516 1.229-2.749 2.751-2.749s2.755 1.233 2.755 2.749c0 1.521-1.233 2.756-2.755 2.756zM9.489 27.271h-4.749v-15.271h4.749zM29.636 0h-27.276c-1.303 0-2.36 1.031-2.36 2.307v27.387c0 1.276 1.057 2.307 2.36 2.307h27.271c1.301 0 2.369-1.031 2.369-2.307v-27.387c0-1.276-1.068-2.307-2.369-2.307z"
          />
        </svg>
      </a>
    </div>
  </div>
</template>

<style scoped>
.glow-card::after {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background: linear-gradient(315deg, #323232, #0d5c3c);
  filter: blur(30px);
  z-index: 0;
  border-radius: 0.75rem;
}

.glow-card > * {
  position: relative;
  z-index: 1;
}
</style>
