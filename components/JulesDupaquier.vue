<template>
    <div class="jules-dupaquier-container">
      <img
        :src="profileImage"
        alt="Photo de profil de Jules Dupaquier"
        class="w-[350px] h-auto rounded-lg shadow-lg"
      />
    </div>
  </template>
  
  <script setup>
  // Importation de l'image depuis le dossier assets
  import profileImage from "@/assets/JulesDupaquier.png";
  </script>
  
  <style scoped>
  .jules-dupaquier-container {
    display: flex;
    justify-content: center;
    align-items: center;
  }
  </style>
  