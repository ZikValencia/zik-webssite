<template>
  <div class="header-wrapper">
    <v-container class="text-center">
      <v-img class="mb-4" height="300" src="@/assets/zik-logo.svg" />
      <v-col cols="12">
        <v-btn
          v-for="item in navItems"
          :key="item.label"
          class="mx-2 text-h4"
          :href="`#${item.id}`"
          size="x-large"
          variant="text"
          @click.prevent="scrollTo(item.id)"
        >
          {{ item.label }}
        </v-btn>
      </v-col>

    </v-container>

  </div>

</template>

<script lang="ts" setup>
  import { ref } from 'vue'

  const navItems = ref([
    { label: 'Home', id: 'home' },
    { label: 'About', id: 'about' },
    { label: 'Skills', id: 'skills' },
    { label: 'Experience', id: 'experience' },
    { label: 'Contact', id: 'contact' },
  ])

  function scrollTo (id: string) {
    const el = document.querySelector(`#${id}`)
    if (el) {
      (el as HTMLElement).scrollIntoView({ behavior: 'smooth' })
    }
  }
</script>

<style scoped>

</style>
