<template>
  <router-link :to="`/spots/${spot.id}`" class="block group">
    <div
      class="bg-white rounded-xl shadow-lg overflow-hidden transition-transform duration-200 transform hover:scale-105"
    >
      <img
        :src="spot.image"
        :alt="spot.name"
        class="w-full h-48 object-cover group-hover:brightness-90"
      />
      <div class="p-4">
        <h2 class="text-xl font-semibold mb-2 text-gray-800">
          {{ spot.name }}
        </h2>
        <p class="text-gray-600 text-sm mb-4 line-clamp-3">
          {{ spot.shortDescription }}
        </p>
        <span class="inline-block text-primary font-semibold"
          >View Details →</span
        >
      </div>
    </div>
  </router-link>
</template>

<script setup>
defineProps({
  spot: Object,
})
</script>
