<script setup>
defineProps({
  education: {
    type: Array,
    default: () => [],
  },
});
</script>

<template>
  <h2 class="text-3xl font-bold text-center text-[#31525B]">Mes formations</h2>
  <div
    v-for="studie in education"
    :key="studie.name"
    class="bg-[#FCFCF0] rounded-lg shadow-md p-6 my-4 border-l-4 border-[#31525B]"
  >
    <h3 class="text-xl font-semibold text-[#31525B] mb-1">
      {{ studie.studyType }} -
      <a
        :href="studie.url"
        target="_blank"
        class="text-[#B3DEE5] hover:underline"
        >{{ studie.institution }}</a
      >
    </h3>
    <p class="text-sm text-gray-500 mb-2">
      du {{ studie.startDate }} au {{ studie.endDate }}
    </p>
    <p class="mb-2">{{ studie.area }}</p>
  </div>
</template>
