<template>
  <div class="card max-w-[300px] mx-auto text-center bg-noir25 p-6 rounded-lg shadow-md hover:shadow-lg transition-transform transform hover:scale-105">
    <!-- Icône -->
    <span class="text-blanc text-[40px]">{{ icon }}</span>

    <!-- Titre -->
    <h3 class="text-xl font-bold text-blanc mt-4">{{ title }}</h3>

    <!-- Description -->
    <p class="text-sm text-disabled mt-2">{{ description }}</p>
  </div>
</template>

<script setup>
// Props pour personnaliser chaque card
defineProps({
  icon: String,
  title: String,
  description: String,
});
</script>
