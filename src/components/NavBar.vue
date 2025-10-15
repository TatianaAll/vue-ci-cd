<script setup lang="ts">
import NavLink from "./NavLink.vue";
</script>

<template>
  <header>
    <nav class="bg-gray-600 text-white p-4">
      <div class="">
        <ul class="relative flex h-10 items-center justify-start gap-8">
          <li class="">
            <NavLink to="#home">Accueil</NavLink>
          </li>
          <li>
            <NavLink to="#profile">Mon profil</NavLink>
          </li>
          <li>
            <NavLink to="#contact">Contact</NavLink>
          </li>
        </ul>
      </div>
    </nav>
  </header>
</template>
