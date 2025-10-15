<script setup>
defineProps({
  basics: {
    type: Object,
    default: () => ({
      name: "",
      label: "",
      image: "",
      email: "",
      phone: "",
      profiles: [],
    }),
  },
});
</script>

<template>
  <div class="flex flex-col items-center text-center py-8">
    <!-- Image de profil -->
    <img
      v-if="basics.image"
      :src="basics.image"
      alt="Photo de profil"
      class="w-32 h-32 rounded-full object-cover shadow-md mb-4"
    />

    <!-- Nom et poste -->
    <h1 class="text-3xl font-bold text-gray-900">{{ basics.name }}</h1>
    <h2 class="text-lg text-gray-600 mb-4">{{ basics.label }}</h2>

    <!-- Contact -->
    <div class="space-y-1 text-gray-700">
      <p v-if="basics.email">
        📧
        <a
          :href="`mailto:${basics.email}`"
          class="text-[#FC6471] hover:underline"
        >
          {{ basics.email }}
        </a>
      </p>
      <p v-if="basics.phone">📞 {{ basics.phone }}</p>
    </div>

    <div
      v-if="basics.profiles?.length"
      class="flex flex-wrap justify-center gap-3 mt-4"
    >
      <a
        v-for="profile in basics.profiles"
        :key="profile.network"
        :href="profile.url"
        target="_blank"
        class="bg-gray-100 hover:bg-[#31525B] hover:text-white transition-colors px-4 py-1.5 rounded-full text-sm font-medium"
      >
        {{ profile.network }}
      </a>
    </div>
  </div>
</template>
