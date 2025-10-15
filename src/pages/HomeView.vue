<script setup>
import ContactComponent from "../components/ContactComponent.vue";
import ProfileView from "../components/ProfileView.vue";
import WorkExperiments from "../components/resume/WorkExperiments.vue";
import resume from "../assets/resume.json";
</script>

<template>
  <main class="p-4 bg-[#FCFCF0]">
    <section id="home" class="bg-[#FAE6B1] rounded-md m-2 p-4">
      <div class="flex items-center justify-around gap-4 mx-auto">
        <div>
          <h1 class="text-5xl font-bold text-center font-lexend text-[#31525B]">
            Tatiana Allery
          </h1>
          <p class="text-3xl font-lexend text-[#31525B]">
            Développeuse web junior
          </p>
        </div>
        <div class="w-[30rem] mt-4 text-xs">
          <img
            src="../assets/homePhoto.jpg"
            alt="c'est pas moi mais presque"
            class="rounded-lg shadow-lg"
          />
          image d'illustration, qui ne reflète aucune réalité 😇
        </div>
      </div>
    </section>

    <section id="profile" class="bg-[#FAE6B1] rounded-md m-2 p-4">
      <ProfileView />
    </section>

    <section id="experiences" class="bg-[#FAE6B1] rounded-md m-2 p-4">
      <WorkExperiments :work="resume.work" />
    </section>

    <section id="contact" class="bg-[#FAE6B1] rounded-md m-2 p-4">
      <ContactComponent />
    </section>
  </main>
</template>
