<template>
  <v-timeline align="start">
    <v-timeline-item
      v-for="(year, i) in years"
      :key="i"
      :dot-color="year.color"
      size="small"
    >
      <template #opposite>
        <div
          :class="`pt-1 headline font-weight-bold text-${year.color}`"
          v-text="year.year"
        />
      </template>
      <div>
        <h2 :class="`mt-n1 headline font-weight-light mb-4 text-${year.color}`">
          My Journey
        </h2>
        <div>
          This journey represents my professional growth and the milestones I've achieved over the years. Each year marks a significant step in my career, showcasing my dedication to continuous learning and improvement.
          From mastering new technologies to leading impactful projects, this timeline reflects my commitment to excellence in software development.
        </div>
      </div>
    </v-timeline-item>
  </v-timeline>
</template>

<script setup>
  const years = [
    {
      color: 'cyan',
      year: '1960',
    },
    {
      color: 'green',
      year: '1970',
    },
    {
      color: 'pink',
      year: '1980',
    },
    {
      color: 'amber',
      year: '1990',
    },
    {
      color: 'orange',
      year: '2000',
    },
  ]
</script>
