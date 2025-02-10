<template>
    <div class="min-h-screen bg-noir text-blanc flex flex-col">
      <!-- Header -->
      <Header />
  
      <!-- Contenu principal -->
      <main class="flex-grow flex flex-col justify-center items-center px-4">
        <!-- Message principal -->
        <h1 class="text-3xl sm:text-4xl md:text-5xl font-bold mb-6 text-center">
          Merci pour votre inscription !
        </h1>
  
        <!-- Sous-titre -->
        <p class="text-lg sm:text-xl md:text-2xl text-center max-w-2xl mb-8">
          Vous serez informé dès que l'application CybGuard sera disponible. En attendant, restez vigilant et protégez vos données en ligne !
        </p>
  
        <!-- Bouton Retour à l'accueil -->
        <NuxtLink to="/" class="btn btn-primary">
          Retour à l'accueil
        </NuxtLink>
      </main>
  
      <!-- Footer -->
      <Footer />
    </div>
  </template>
  
  <script setup>
  // Importation des composants Header et Footer
  import Header from "@/components/Header.vue";
  import Footer from "@/components/Footer.vue";
  </script>
  
  <style scoped>
  /* Styles spécifiques à la page */
  </style>
  