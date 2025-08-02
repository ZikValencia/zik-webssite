<template>
  <v-main>
    <Header />
    <router-view class="main-container" />
  </v-main>

  <AppFooter />
</template>

<style scoped>
.main-container {
  max-width: 1580px;      /* Narrower layout */
}
</style>
