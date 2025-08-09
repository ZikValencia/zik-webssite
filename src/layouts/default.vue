<template>
  <v-main>
    <Header />
    <v-container class="main-container" fluid>
      <v-card>
        <router-view class="main-container " />
      </v-card>

    </v-container>
  </v-main>

  <AppFooter />
</template>

<style scoped>
.main-container {
  max-width: 1580px;      /* Narrower layout */
}
</style>
