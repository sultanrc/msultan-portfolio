<script setup>
import { ref } from 'vue'
import LeftColumn from './components/LeftColumn.vue'
import RightColumn from './components/RightColumn.vue'

const activeTab = ref('about')

const scrollToSection = (sectionId) => {
  const section = document.getElementById(sectionId)
  if (section) {
    section.scrollIntoView({ behavior: 'smooth' })
  }
}

const updateActiveTab = (section) => {
  activeTab.value = section
}
</script>
<template>
  <main class="mx-auto max-w-full font-comfortaa overflow-hidden">
    <section class="flex flex-col lg:flex-row h-full lg:mx-16 2xl:mx-60">
      <div class="left-column lg:w-6/12 lg:flex 2xl:ml-14 h-full hidden">
        <LeftColumn :activeTab="activeTab" @tab-click="scrollToSection" />
      </div>
      <div class="right-column lg:w-6/12 h-full">
        <RightColumn @scroll-update="updateActiveTab" />
      </div>
    </section>
  </main>
</template>

<style scoped>
@media (min-width: 1280px) {
  .left-column {
    transform: perspective(1000px) rotateY(10deg);
    transform-origin: center right;
  }

  .right-column {
    transform: perspective(1000px) rotateY(-10deg);
    transform-origin: center left;
  }
}
</style>
