<script setup>
import NavBar from "./components/NavBar.vue";
import WorkExperiments from "./components/resume/WorkExperiments.vue";
import HomeView from "./pages/HomeView.vue";
import resume from "./assets/resume.json";
</script>

<template>
  <NavBar />
  <HomeView />
  <WorkExperiments :work="resume.work" />
</template>

<style scoped></style>
