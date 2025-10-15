<template>
  <a :href="'#' + to" @click="emit('activate', to)" :class="[
    'transition hover:text-gray-300',
    active ? 'text-xl text-gray-300' : ''
  ]">
    <slot />
  </a>
</template>