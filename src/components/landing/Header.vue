<template>
  <div class="header-wrapper">
    <v-container class="text-center">
      <v-img class="mb-4" height="300" src="@/assets/zik-logo.svg" />
      <v-col cols="12">
        <v-btn
          v-for="item in ['Home','Skills', 'Experience', 'Projects', 'More About Me','Contact']"
          :key="item"
          class="mx-2 text-h5"
          size="x-large"
          :to="`/${item.toLowerCase()}`"
          variant="text"
        >
          {{ item }}
        </v-btn>
      </v-col>

    </v-container>

  </div>

</template>

<script lang="ts" setup>
  //
</script>

<style scoped>

</style>
