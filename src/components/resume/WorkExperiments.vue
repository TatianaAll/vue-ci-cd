<script setup>
defineProps({
  work: {
    type: Array,
    default: () => [],
  },
});
</script>

<template>
  <h2 class="text-3xl font-bold text-center text-[#31525B]">
    Mes différentes expériences professionnelles
  </h2>
  <div
    v-for="job in work"
    :key="job.name"
    class="bg-[#FCFCF0] rounded-lg shadow-md p-6 my-4 border-l-4 border-[#31525B]"
  >
    <h3 class="text-xl font-semibold text-[#31525B] mb-1">
      {{ job.position }} -
      <a
        :href="job.url"
        target="_blank"
        class="text-[#FC6471] hover:underline"
        >{{ job.name }}</a
      >
    </h3>
    <p class="text-sm text-gray-500 mb-2">
      {{ job.startDate }} à {{ job.endDate }}
    </p>
    <p class="mb-2">{{ job.summary }}</p>
    <ul class="list-disc list-inside space-y-1 text-gray-700">
      <li v-for="highlight in job.highlights" :key="highlight">
        {{ highlight }}
      </li>
    </ul>
  </div>
</template>
