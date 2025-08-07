<template>

  <v-container class="text-center py-8" max-width="1230px">
    <h1 class="text-h3 font-weight-bold gradient-text">My Journey 🚀</h1>
    <p class="text-h5  mt-2">
      This journey represents my professional growth and the milestones I've achieved over the years. Each year marks a significant step in my career, showcasing my dedication to continuous learning and improvement.
    </p>
  </v-container>
  <v-divider class="ma-8" />
  <v-timeline align="start">
    <v-timeline-item
      v-for="(year, i) in years"
      :key="i"
      class="my-12"
      :dot-color="year.color"
      size="small"
    >
      <template #opposite>
        <div
          :class="`pt-1 headline font-weight-bold text-${year.color} text-${i % 2 === 0 ? 'right' : 'left'} text-h6`"
          v-text="year.year"
        />
      </template>

      <v-card
        class="timeline-item pa-4 mb-6"
        rounded="lg"
      >
        <div :class="`text-${i % 2 === 0 ? 'left' : 'right'}`">
          <h2 class="mt-n1 headline font-weight-light mb-4">
            {{ year.description }}
          </h2>
          <div>
            {{ year.place }}
          </div>
        </div>
      </v-card>
    </v-timeline-item>
  </v-timeline>
  <v-divider class="ma-8" />
</template>

<script setup>
  const years = [
    {
      description: 'Graduated with a degree in Information Technology, Bachelor of Science in Information Technology',
      place: 'Silliman University, Dumaguete City.',
      year: '🎓 2016– 2021',
    },
    {
      description: 'While finishing my degree, worked as a customer service representative. Developing strong communication skills and a customer-centric mindset.',
      place: 'Qualfon, Dumaguete City Branch',
      year: 'March 2020 – January 2021',
    },
    {
      year: 'January 2021 – April 2021',
      place: 'Perti Solution Inc. Vancouver Canada BC',
      description: 'Internship as a Web development and Search Engine Optimization (SEO) Specialist.',
    },

    {
      year: 'January 2021 – August 2021',
      place: 'Perti Solution Inc. Vancouver Canada BC',
      description: 'I worked as a Technical Consultant and Frontend Web Developer specializing in building and maintaining websites for clients.',
    },
    {
      year: 'August 2021 - Present',
      place: 'Mobile Internet Technology co., Ltd. Tokyo Japan',
      description: 'I Software Engineer specializing in building and maintaining web applications and IOS Applications.',
    },
  ]
</script>

<style scoped>
  .timeline-item {
    background: linear-gradient(
      185deg,
      rgba(40, 40, 40, 1),       /* matte dark grey */
      rgba(0, 162, 140, 0.1),    /* soft teal hint */
      rgba(25, 25, 25, 1)        /* deep matte base */
    );
    max-width: 570px;
  }
  </style>
