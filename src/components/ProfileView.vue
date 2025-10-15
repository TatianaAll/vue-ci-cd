<template>
  <div class="p-4">
    <h1 class="text-3xl font-bold text-center text-[#31525B]">
      {{ datas.basics.summary }}
    </h1>
    <div class="text-center my-4">
      A propos de moi : <br />
      <p></p>
      Mon nom est {{ datas.basics.name }}, j'ai 28 ans. Je suis
      {{ datas.basics.label }}. J'ai commencé ma formation en alternance le
      {{ datas.education[0].startDate }} à {{ datas.education[0].institution }},
      je suis en alternance chez {{ datas.work[0].name }}. J'habite à
      {{ datas.basics.location.address }}, {{ datas.basics.location.city }}.
    </div>
  </div>
</template>
<script setup>
import datas from "../assets/resume.json";
</script>
