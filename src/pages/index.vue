<template>
  <div>
    <section id="about"><About /></section>
    <section id="skills"><Skills /></section>
    <section id="experience"><TimeLineSection /></section>
    <section id="contact"><ContactInfo /></section>
  </div>
</template>

<script setup lang="ts">
  import About from '@/components/landing/About.vue'
  import ContactInfo from '@/components/landing/ContactInfo.vue'
  import Skills from '@/components/landing/Skills.vue'
  import TimeLineSection from '@/components/landing/TimeLineSection.vue'
</script>
