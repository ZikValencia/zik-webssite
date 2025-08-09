<template>
  <v-divider class="ma-8" />
  <v-container class="text-center py-8">
    <h1 class="text-h3 font-weight-bold gradient-text">My Development Toolkit 🛠️</h1>
    <p class="text-h5  mt-2">
      A collection of tools and technologies I use or have worked with
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
        md="6"
        sm="12"
        xs="12"
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
          <div class="text-h6 mt-2 text-center  ">{{ tech.name }}</div>
          <div class="text-subtitle-1 mt-1 text-center">{{ tech.description }}</div>
        </v-card>
      </v-col>
    </v-row>
  </v-container>
  <v-divider class="ma-8" />
</template>

<script setup lang="ts">
  const techStack = [
    {
      name: 'swift',
      icon: 'mdi-language-swift',
      color: '#f05138',
      description: 'Swift for iOS development, building native mobile applications with a focus on performance and user experience.',
    },
    {
      name: 'swiftui',
      icon: 'mdi-language-swift',
      color: '#f05138',
      description: 'SwiftUI for declarative UI development in iOS, enabling responsive and adaptive interfaces with less code.',
    },
    {
      name: 'HTML5',
      icon: 'mdi-language-html5',
      color: '#e34c26',
      description: 'HTML5 for semantic, accessible web content and responsive layouts.',
    },
    {
      name: 'CSS3',
      icon: 'mdi-language-css3',
      color: '#1572b6',
      description: 'CSS3 for styling web applications with modern design principles and responsive design.',
    },
    {
      name: 'Sass',
      icon: 'mdi-sass',
      color: '#cc6699',
      description: 'Sass for modular, maintainable CSS with variables, nesting, and mixins.',
    },
    {
      name: 'Tailwind CSS',
      icon: 'mdi-tailwind',
      color: '#38bdf8',
      description: 'Tailwind CSS for utility-first styling, enabling rapid UI development with custom themes.',
    },
    {
      name: 'Bootstrap',
      icon: 'mdi-bootstrap',
      color: '#563d7c',
      description: 'Bootstrap for responsive, mobile-first web design with pre-built components.',
    },
    {
      name: 'Vue.js',
      icon: 'mdi-vuejs',
      color: '#42b883',
      description: 'Vue.js front-end framework for building responsive, modular single-page applications (SPAs) and admin dashboards.',
    },
    {
      name: 'TypeScript',
      icon: 'mdi-language-typescript',
      color: '#3178c6',
      description: 'TypeScript for type-safe, scalable JavaScript development in modern Vue 3 and Node.js projects.',
    },
    {
      name: 'JavaScript',
      icon: 'mdi-language-javascript',
      color: '#f7df1e',
      description: 'JavaScript for dynamic, client-side scripting in web applications, enhancing user experiences and interactivity.',
    },
    {
      name: 'Node.js',
      icon: 'mdi-nodejs',
      color: '#83cd29',
      description: 'Node.js runtime for creating fast, scalable server-side APIs, CLI tools, and real-time applications.',
    },
    {
      name: 'Go (Golang)',
      icon: 'mdi-language-go',
      color: '#00add8',
      description: 'Golang backend development with Gin framework for high-performance REST APIs and cloud-native services.',
    },
    {
      name: 'Docker',
      icon: 'mdi-docker',
      color: '#2496ed',
      description: 'Docker containerization for consistent deployment of Vue.js, Node.js, and Go applications on AWS and GCP.',
    },
    {
      name: 'Amazon Web Services (AWS)',
      icon: 'mdi-aws',
      color: '#ff9900',
      description: 'AWS cloud solutions for hosting, CI/CD, serverless applications, and scalable infrastructure.',
    },
    {
      name: 'Vuetify',
      icon: 'mdi-vuetify',
      color: '#1867c0',
      description: 'Vuetify UI library for Vue.js, enabling mobile-first responsive design and material design compliance.',
    },
    {
      name: 'Element Plus',
      icon: 'mdi-alpha-e-circle-outline', // No direct MDI icon; using "E" icon
      color: '#67c23a',
      description: 'Element Plus UI framework for Vue 3, providing high-quality, customizable component libraries.',
    },
    {
      name: 'GitHub',
      icon: 'mdi-github',
      color: '#000000',
      description: 'GitHub for version control, collaborative development, CI/CD pipelines, and code hosting.',
    },
    {
      name: 'MySQL',
      icon: 'mdi-database',
      color: '#4479a1',
      description: 'MySQL relational database for enterprise applications, optimized with stored procedures and indexing.',
    },
    {
      name: 'PostgreSQL',
      icon: 'mdi-database',
      color: '#336791',
      description: 'PostgreSQL advanced SQL database with Prisma ORM for type-safe, performant data access.',
    },
    {
      name: 'WordPress',
      icon: 'mdi-wordpress',
      color: '#21759b',
      description: 'WordPress CMS for custom themes, SEO-friendly blogging, and plugin-based site customization.',
    },
    {
      name: 'Wix',
      icon: 'mdi-web', // No official Wix icon; using a generic web icon
      color: '#000000',
      description: 'Wix website builder for creating mobile-friendly, drag-and-drop customizable websites.',
    },
    {
      name: 'Squarespace',
      icon: 'mdi-web', // No official Squarespace icon; generic web icon
      color: '#000000',
      description: 'Squarespace platform for visually appealing, responsive websites with integrated e-commerce.',
    },

  ]

</script>

<style scoped>

</style>
