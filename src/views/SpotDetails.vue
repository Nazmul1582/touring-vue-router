<script setup>
import { useRoute, useRouter } from "vue-router"
import { spots } from "@/data/spots"
import { computed } from "vue"

const route = useRoute()
const router = useRouter()

const spot = computed(() =>
  spots.find((s) => s.id === parseInt(route.params.id))
)
</script>

<template>
  <div v-if="spot" class="max-w-4xl mx-auto px-4 py-8">
    <h1 class="text-4xl font-bold mb-4 text-balance">{{ spot.title }}</h1>
    <img
      :src="spot.image"
      alt=""
      class="rounded-xl shadow-lg mb-6 w-full h-80 object-cover"
    />
    <p class="text-lg mb-6 leading-relaxed">{{ spot.longDescription }}</p>
    <button
      @click="router.back()"
      class="bg-blue-600 text-white px-6 py-2 rounded-xl hover:bg-blue-700 cursor-pointer"
    >
      ← Back
    </button>
  </div>
  <div v-else class="text-center mt-16 text-red-500">
    <p>Tourist spot not found.</p>
  </div>
</template>
