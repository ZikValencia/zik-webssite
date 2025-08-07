<template>
  <div>
    <section id="about"><About /></section>
    <section id="skills"><Skills /></section>
    <section id="experience"><TimeLine /></section>
    <section id="contact"><ContactInfo /></section>
  </div>
</template>

<script setup lang="ts">
  import About from '@/components/landing/About.vue'
  import ContactInfo from '@/components/landing/ContactInfo.vue'
  import Skills from '@/components/landing/Skills.vue'
  import TimeLine from '@/components/landing/TimeLine.vue'
</script>
