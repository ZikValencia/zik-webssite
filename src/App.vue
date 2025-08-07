<template>
  <v-app>
    <router-view />
    <button
      v-show="showButton"
      aria-label="Back to top"
      class="back-to-top"
      @click="scrollToTop"
    >
      <v-icon>mdi-arrow-up</v-icon>
    </button>
  </v-app>
</template>

<script lang="ts" setup>

  import { onMounted, onUnmounted, ref } from 'vue'

  const showButton = ref(false)

  function scrollToTop () {
    window.scrollTo({ top: 0, behavior: 'smooth' })
  }

  function handleScroll () {
    showButton.value = window.scrollY > 300
  }

  onMounted(() => {
    window.addEventListener('scroll', handleScroll)
  })

  onUnmounted(() => {
    window.removeEventListener('scroll', handleScroll)
  })
</script>

<style>
.back-to-top {
  position: fixed;
  bottom: 4rem;
  right: 2rem;
  background-color: #00a28c;
  color: white;
  border: none;
  border-radius: 50%;
  width: 3rem;
  height: 3rem;
  font-size: 1.5rem;
  box-shadow: 0 4px 10px rgba(0, 0, 0, 0.3);
  cursor: pointer;
  z-index: 999;
  transition: opacity 0.3s ease;
}

.back-to-top:hover {
  background-color: #008f7a;
}

html {
  scroll-behavior: smooth;
}
</style>
