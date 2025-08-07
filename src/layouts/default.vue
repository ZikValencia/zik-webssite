<template>
  <v-main>

    <v-container class="main-container" fluid>
      <v-card class="pa-6" padding="10">
        <Header />
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
