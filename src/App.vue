<template>
  <div class="min-h-screen bg-gray-50">
    <header class="flex justify-center gap-6 p-4 bg-white shadow">
      <RouterLink to="/" class="text-blue-600 hover:underline">Home</RouterLink>
      <RouterLink to="/about" class="text-green-600 hover:underline"
        >About</RouterLink
      >
    </header>
    <main>
      <RouterView />
    </main>
  </div>
</template>

<script setup>
import { RouterLink, RouterView } from "vue-router"
</script>
