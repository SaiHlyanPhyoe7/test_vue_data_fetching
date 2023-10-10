<script setup lang="ts">
import { RouterLink, RouterView } from 'vue-router'
</script>

<template>
  <header>
    <nav class="flex justify-around text-indigo-200 bg-indigo-400 items-center">
      <RouterLink
        :class="{ 'text-yellow-400 scale-110 duration-700': $route.path === '/' }"
        to="/"
        class="hover:underline py-4 underline-offset-2 hover:text-indigo-100 cursor-pointer"
        >Home</RouterLink
      >
      <RouterLink
        :class="{
          'text-yellow-400 scale-110 duration-700': $route.path === '/about'
        }"
        to="/about"
        class="hover:underline py-4 underline-offset-2 hover:text-indigo-100 cursor-pointer"
        >About</RouterLink
      >
    </nav>
  </header>

  <RouterView />
</template>
