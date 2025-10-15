<script setup>
import ContactComponent from "../components/ContactComponent.vue";
import ProfileView from "../components/ProfileView.vue";
</script>

<template>
  <main class="p-4 bg-gray-100 h-[100vh] scroll-smooth">
    <section id="home">
      <h1 class="text-3xl font-bold text-center">
        Bienvenue sur mon portfolio !
      </h1>
      <p class="mt-4 text-center">Ceci est ma page d'accueil.</p>
    </section>
    <section id="profile">
      <ProfileView />
    </section>
    <section id="contact">
      <ContactComponent />
    </section>
  </main>
</template>
