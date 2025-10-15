<script setup>
defineProps({
  work: {
    type: Array,
    default: () => [],
  },
});
</script>

<template>
  <section>
    <h2>Mes différentes expériences professionnelles</h2>
    <div v-for="job in work" :key="job.name" class="mb-1">
      <h3>
        {{ job.position }} -
        <a :href="job.url" target="_blank">{{ job.name }}</a>
      </h3>
      <p>{{ job.startDate }} à {{ job.endDate }}</p>
      <p>{{ job.summary }}</p>
      <ul>
        <li v-for="highlight in job.highlights" :key="highlight">
          {{ highlight }}
        </li>
      </ul>
    </div>
  </section>
</template>
