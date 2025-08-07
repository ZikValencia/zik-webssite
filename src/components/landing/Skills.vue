<template>
  <v-divider class="ma-8" />
  <v-container class="text-center py-8">
    <h1 class="text-h3 font-weight-bold gradient-text">My Tech Stack</h1>
    <p class="text-h5  mt-2">
      Tools and technologies I use to build modern web applications
    </p>
  </v-container>
  <v-container class="d-flex  justify-center" fluid>

    <v-row
      class="w-100"
      gutter="20px"
      style="max-width: 1230px;"
    >

      <v-col
        v-for="tech in techStack"
        :key="tech.name"
        cols="4"
      >
        <v-card
          class="d-flex flex-column align-center justify-center  pa-4 fill-height"
          rounded="lg"
          style="background: linear-gradient(
            185deg,
            rgba(0, 162, 140, 0.1),      /* light teal */
            rgba(0, 162, 140, 0.3),      /* deeper teal */
            rgba(55, 55, 55, 0.5)        /* dark grey */
            );
            ; "
        >
          <v-icon :color="tech.color" :icon="tech.icon" :size="60" />
          <div class="text-h6 mt-2">{{ tech.name }}</div>
          <div class="text-subtitle-1 mt-1">{{ tech.description }}</div>
        </v-card>
      </v-col>
    </v-row>
  </v-container>
</template>

<script setup lang="ts">
  const techStack = [
    {
      name: 'Vue.js',
      icon: 'mdi-vuejs',
      color: '#42b883',
      description: 'My primary front-end framework for building modular admin tools and SPA dashboards.',
    },
    {
      name: 'TypeScript',
      icon: 'mdi-language-typescript',
      color: '#3178c6',
      description: 'Used across all projects to ensure strong type safety, especially in large Vue 3 codebases.',
    },
    {
      name: 'Node.js',
      icon: 'mdi-nodejs',
      color: '#83cd29',
      description: 'Used for server-side tools and utilities, mainly for CLI scripts and data processing.',
    },
    {
      name: 'Go',
      icon: 'mdi-language-go',
      color: '#00add8',
      description: 'Backend language of choice for building performant APIs with Gin and Lambda on AWS.',
    },
    {
      name: 'Docker',
      icon: 'mdi-docker',
      color: '#2496ed',
      description: 'Used to containerize Go APIs and Vue apps for GCP/AWS deployment (ECS, Cloud Run).',
    },
    {
      name: 'AWS',
      icon: 'mdi-aws',
      color: '#ff9900',
      description: 'Deploy Lambda, API Gateway, Cognito, and S3 for scalable authentication and storage.',
    },
    {
      name: 'Vuetify',
      icon: 'mdi-vuetify',
      color: '#1867c0',
      description: 'UI framework for Vue 3 admin interfaces and mobile-first layouts in CrewAssist apps.',
    },
    {
      name: 'GitHub',
      icon: 'mdi-github',
      color: '#000000',
      description: 'Version control, CI/CD workflows, commit conventions, and private repo hosting.',
    },
    {
      name: 'MySQL',
      icon: 'mdi-database',
      color: '#4479a1',
      description: 'Used with stored procedures, dynamic ACLs, and employee data for enterprise apps.',
    },
  ]
</script>

<style scoped>

</style>
