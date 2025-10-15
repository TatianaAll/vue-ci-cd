<script setup>
import { ref } from "vue";
const showHello = () => {
  ref("Hello from HomeView");
};
</script>
<template>
  <h1>Home view</h1>
  <button @click="showHello">Click me</button>
</template>
