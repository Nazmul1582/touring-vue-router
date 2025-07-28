<script setup>
import SpotCard from "@/components/SpotCard.vue"
import { spots } from "@/data/spots"
</script>

<template>
  <section class="p-6 container mx-auto">
    <h1 class="text-4xl font-bold text-center mb-8">Explore Bangladesh</h1>

    <div class="grid gap-4 sm:grid-cols-2 md:grid-cols-3 xl:grid-cols-4">
      <SpotCard v-for="spot in spots" :key="spot.id" :spot="spot" />
    </div>
  </section>
</template>
