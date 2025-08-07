<template>
  <v-container class="">
    <!-- Hero Section -->

    <v-row class="flex-wrap-reverse">
      <v-spacer />
      <v-col class="text-center" cols="12" md="4">
        <div class="glow-container">
          <v-img
            alt="Zik profile image"
            class="glow-image"
            cover
            height="auto"
            src="@/assets/image/self.png"
            width="500"
          />
        </div>
      </v-col>
      <v-col class="d-flex flex-column justify-center" cols="12" md="6">
        <v-card class="pa-6" color="teal-darken-4 darken-5" rounded="lg">

          <h1 class="text-h2 font-weight-bold mb-2">
            Hi, I'm <span class="text-primary">Zik</span> 👋
          </h1>

          <h2 class="text-h4 text-grey-lighten-1 mb-4 font-weight-regular">
            Filipino full-stack developer based in Japan 🇯🇵
          </h2>

          <p class="text-h6 text-grey-lighten-1 mb-6">
            I specialize in building scalable web applications and cloud-native solutions. With a passion for clean architecture and efficient workflows, I create software that delivers real-world impact.
          </p>
        </v-card></v-col>
      <v-spacer />
    </v-row>

  </v-container>
</template>

<script lang="ts" setup>
  const items = [
    {
      color: 'red-lighten-2',
      icon: 'mdi-star',
    },
    {
      color: 'purple-lighten-2',
      icon: 'mdi-book-variant',
    },
    {
      color: 'green-lighten-1',
      icon: 'mdi-airballoon',
    },
    {
      color: 'indigo-lighten-2',
      icon: 'mdi-layers-triple',
    },
  ]
</script>

<style scoped>
  .glow-container {
  position: relative;
  display: inline-block;
}

.glow-container::before {
  content: "";
  position: absolute;
  top: 50%;
  left: 50%;
  width: 120%;
  height: 120%;
  transform: translate(-50%, -50%);
  background: radial-gradient(circle, rgba(0, 191, 165, 0.5) 0%, transparent 70%);
  filter: blur(60px);
  z-index: 0;
  pointer-events: none;
}

</style>
