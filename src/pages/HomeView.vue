<script setup>
import ContactComponent from "../components/ContactComponent.vue";
import ProfileView from "../components/ProfileView.vue";
</script>

<template>
  <main class="p-4 scroll-smooth">
    <section id="home" class="bg-gray-100 rounded-xsm m-2 p-4">
      <div class="flex items-center justify-around gap-4 mx-auto">
        <div>
          <h1 class="text-5xl font-bold text-center font-lexend">
            Tatiana Allery
          </h1>
          <p class="text-3xl font-lexend">Développeuse web junior</p>
        </div>
        <div class="w-[30rem] mt-4">
          <img
            src="../assets/homePhoto.jpg"
            alt="c'est pas moi mais presque"
            class="rounded-lg shadow-lg"
          />
        </div>
      </div>
    </section>

    <section id="profile" class="bg-gray-100">
      <ProfileView />
    </section>

    <section id="contact" class="bg-gray-100">
      <ContactComponent />
    </section>
  </main>
</template>
