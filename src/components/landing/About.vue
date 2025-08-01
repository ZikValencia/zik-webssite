<template>
  <v-container class="py-16">
    <!-- Hero Section -->
    <v-row align="center" justify="space-between" class="flex-wrap-reverse">
      <!-- Left Text Content -->
      <v-col cols="12" md="7">
        <h1 class="text-h2 font-weight-bold mb-4">Hi, I'm Zik 👋</h1>
        <p class="text-body-1 text-grey-darken-2 mb-6">
          Welcome to <strong>ZIK STUDIOS</strong> — my creative and technical playground.
          I'm a developer, designer, and builder passionate about crafting thoughtful digital
          experiences. Whether it's scalable backends, pixel-perfect interfaces, or AI-driven tools,
          I love bringing ideas to life with code.
        </p>

        <v-btn color="primary" size="large" class="mt-2" rounded>
          Check Out My Work
        </v-btn>
      </v-col>

      <!-- Right Image Content -->
      <v-col cols="12" md="5" class="text-center">
        <v-img
          src="https://via.placeholder.com/400x400.png?text=Zik+Profile"
          alt="Zik profile image"
          max-width="300"
          class="rounded-circle mx-auto"
        />
      </v-col>
    </v-row>

    <!-- Divider -->
    <v-divider class="my-12" />

    <!-- About Me Section -->
    <v-row>
      <v-col cols="12" md="10" class="mx-auto">
        <h2 class="text-h5 font-weight-bold mb-4">About Me</h2>
        <p class="text-body-1 text-grey-darken-1">
          I'm a full-stack developer based in Japan, passionate about turning complex
          problems into elegant solutions. I specialize in building scalable web platforms
          with Vue, Go, and modern cloud architectures — and I love automating workflows,
          optimizing performance, and exploring AI-powered applications.
          <br /><br />
          Outside of code, you’ll probably find me exploring side projects, cooking up healthy
          meals, or diving into new tech trends. I believe in continuous learning, building with purpose,
          and sharing what I learn along the way.
        </p>
      </v-col>
    </v-row>
  </v-container>
</template>

<script lang="ts" setup>
// No logic needed for this static page
</script>
