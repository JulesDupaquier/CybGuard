<template>
    <div class="min-h-screen bg-noir text-blanc flex flex-col">
      <!-- Header -->
      <Header />
  
      <!-- Contenu principal -->
      <main class="flex-grow flex flex-col justify-center items-center px-4">
        <!-- Titre principal -->
        <h1 class="text-3xl sm:text-4xl md:text-5xl font-bold mb-6 text-center">
          Rejoignez la liste d'attente pour CybGuard
        </h1>
  
        <!-- Sous-titre -->
        <p class="text-lg sm:text-xl md:text-2xl text-center max-w-2xl mb-8">
          Soyez parmi les premiers à découvrir notre application et à protéger vos données en ligne.
        </p>
  
        <!-- Formulaire d'inscription -->
        <form @submit.prevent="handleSubmit" class="w-full max-w-md bg-noir25 p-6 rounded-lg shadow-lg">
          <!-- Champ e-mail -->
          <div class="mb-4">
            <label for="email" class="block text-sm font-medium mb-2">Votre adresse e-mail :</label>
            <input
              v-model="email"
              type="email"
              id="email"
              placeholder="exemple@email.com"
              required
              class="w-full px-4 py-2 rounded-lg bg-noir text-blanc border border-gray-300 focus:outline-none focus:ring-2 focus:ring-green focus:border-green"
            />
          </div>
  
          <!-- Bouton d'inscription -->
          <button
            type="submit"
            class="btn btn-primary w-full mt-4"
          >
            S'inscrire
          </button>
        </form>
      </main>
  
      <!-- Footer -->
      <Footer />
    </div>
  </template>
  
  <script setup>
  // Importation des composants Header et Footer
  import Header from "@/components/Header.vue";
  import Footer from "@/components/Footer.vue";
  
  // Importation des outils Vue Router
  import { ref } from "vue";
  import { useRouter } from "vue-router";
  
  // Champs réactifs
  const email = ref(""); // Champ e-mail
  
  // Utilisation de Vue Router pour la redirection
  const router = useRouter();
  
  // Fonction pour gérer la soumission du formulaire
  const handleSubmit = () => {
    if (email.value) {
      // Stocker l'adresse e-mail dans localStorage (simulé)
      const waitlist = JSON.parse(localStorage.getItem("waitlist")) || [];
      waitlist.push(email.value);
      localStorage.setItem("waitlist", JSON.stringify(waitlist));
  
      // Afficher l'adresse e-mail dans la console (pour simuler une action backend)
      console.log("Nouvelle inscription :", email.value);
  
      // Réinitialiser le champ e-mail
      email.value = "";
  
      // Rediriger vers la page de confirmation
      router.push("/confirmation");
    }
  };
  </script>
  
  <style scoped>
  /* Styles spécifiques à la page */
  </style>
  