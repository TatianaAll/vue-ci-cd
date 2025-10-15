<template>
  <div class="p-4">
    <h1 class="text-3xl font-bold text-center text-[#31525B]">Me contacter</h1>
    <p class="text-center my-4">
      Vous pouvez me contacter à l'adresse :
      <span class="text-[#31525B] text-bold">{{ datas.basics.email }} </span>
      <br />
      ou par téléphone au
      <span class="text-[#31525B] text-bold">{{ datas.basics.phone }}</span>
    </p>
  </div>
</template>

<script setup>
import datas from "../assets/resume.json";
</script>
