<template>
    <div class="card">
      <!-- Icône -->
      <span class="text-blanc text-[40px]">{{ icon }}</span>
  
      <!-- Titre -->
      <h3>{{ title }}</h3>
  
      <!-- Description -->
      <p>{{ description }}</p>
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
  