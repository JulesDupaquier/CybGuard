<template>
  <div class="quishing-container">
    <img
      :src="quishingImage"
      alt="Infographie Quishing"
      class="w-full h-auto max-w-[400px] mx-auto"
    />
  </div>
</template>

<script setup>
// Importation de l'image depuis le dossier assets
import quishingImage from "@/assets/quishing.png";
</script>

<style scoped>
.quishing-container {
  display: flex;
  justify-content: center;
  align-items: center;
}
</style>
