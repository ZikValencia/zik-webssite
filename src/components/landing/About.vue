<template>
  <v-container class="">
    <!-- Hero Section -->
    <v-row align="center" class="flex-wrap-reverse" justify="space-between">
      <v-col class="text-center" cols="12" md="6">
        <v-img
          alt="Zik profile image"
          class="rounded-circle mx-auto"
          max-width="500"
          src="@/assets/image/self.png"
        />
      </v-col>
      <v-col class="d-flex flex-column justify-center" cols="12" md="6">
        <h1 class="text-h2 font-weight-bold mb-2">
          Hi, I'm <span class="text-primary">Zik</span> 👋
        </h1>

        <h2 class="text-h5 text-grey-darken-1 mb-4 font-weight-regular">
          Filipino full-stack developer based in Japan 🇯🇵
        </h2>

        <p class="text-body-1 text-grey-darken-2 mb-6">
          I specialize in building scalable web applications and cloud-native solutions. With a passion for clean architecture and efficient workflows, I create software that delivers real-world impact.
        </p>

        <v-btn
          class="align-self-start"
          color="primary"
          elevation="2"
          rounded
          size="large"
          to="/projects"
          variant="flat"
        >
          🚀 Check Out My Work
        </v-btn>
      </v-col>

    </v-row>
  </v-container>
  <v-timeline align="start">
    <v-timeline-item
      v-for="(item, i) in items"
      :key="i"
      :dot-color="item.color"
      fill-dot
      :icon="item.icon"
    >
      <v-card>
        <v-card-title :class="['text-h6', `bg-${item.color}`]">
          Lorem Ipsum Dolor
        </v-card-title>
        <v-card-text class="bg-white text--primary">
          <p>Lorem ipsum dolor sit amet, no nam oblique veritus. Commune scaevola imperdiet nec ut, sed euismod convenire principes at. Est et nobis iisque percipit, an vim zril disputando voluptatibus, vix an salutandi sententiae.</p>
          <v-btn
            :color="item.color"
            variant="outlined"
          >
            Button
          </v-btn>
        </v-card-text>
      </v-card>
    </v-timeline-item>
  </v-timeline>
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
