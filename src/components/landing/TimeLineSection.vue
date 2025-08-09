<template>
  <v-container class="py-8" max-width="900">
    <h1 class="text-h5 text-center mb-4">My Journey 🚀</h1>

    <!-- Make the line & dots explicit so they don't disappear on dark bg -->
    <v-timeline
      align="start"
      density="comfortable"
      line-color="teal"
      line-inset="12"
      :side="smAndUp ? 'both' : undefined"
    >
      <v-timeline-item
        v-for="(y, i) in years"
        :key="i"
        dot-color="teal"
        fill-dot
        size="small"
      >
        <!-- Only show 'opposite' when side='both' -->
        <template v-if="smAndUp" #opposite>
          <div class="text-subtitle-1 font-weight-bold">
            {{ y.year }}
          </div>
        </template>

        <div class="pa-6 mt-6" rounded="lg">
          <!-- On mobile, show year inside thdiv -->
          <v-chip
            v-if="!smAndUp"
            class="mb-2"
            color="teal"
            label
            size="small"
          >
            {{ y.year }}
          </v-chip>

          <div class="text-body-1 mb-2">
            {{ y.description }}
          </div>
          <div class="text-medium-emphasis">
            {{ y.place }}
          </div>
        </div>
      </v-timeline-item>
    </v-timeline>
  </v-container>
</template>

<script setup lang="ts">
  import { useDisplay } from 'vuetify'
  const { smAndUp } = useDisplay()

  const years = [
    {
      description: 'Graduated with a degree in Information Technology, Bachelor of Science in Information Technology',
      place: 'Silliman University, Dumaguete City.',
      year: ' 2016– 2021',
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
