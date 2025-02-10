<template>
  <footer class="bg-noir text-blanc py-8">
    <!-- Mention pédagogique -->
    <div class="border-b border-vert pb-4 mb-4">
      <p class="text-center text-sm text-disabled">
        Projet fictif et pédagogique réalisé dans un cadre universitaire.
      </p>
    </div>

    <!-- Contenu principal -->
    <div class="container mx-auto px-6 flex flex-col items-center text-center space-y-6">
      <!-- Liens sociaux -->
      <div class="flex space-x-6">
        <!-- Lien Instagram -->
        <a
          href="https://www.instagram.com/cybguard.app"
          target="_blank"
          rel="noopener noreferrer"
          aria-label="Instagram"
          class="text-blanc hover:text-green transition-colors"
        >
          <svg
            xmlns="http://www.w3.org/2000/svg"
            fill="none"
            viewBox="0 0 24 24"
            stroke-width="2"
            stroke="currentColor"
            class="w-6 h-6"
          >
            <path
              stroke-linecap="round"
              stroke-linejoin="round"
              d="M7.75 3h8.5A4.75 4.75 0 0 1 21 7.75v8.5A4.75 4.75 0 0 1 16.25 21h-8.5A4.75 4.75 0 0 1 3 16.25v-8.5A4.75 4.75 0 0 1 7.75 3zm10.25 4a1.25 1.25 0 1 1-2.5-.001A1.25 1.25 0 0 1 18 7zm-6 .5a4.5 4.5 0 1 0 .001 9A4.5 4.5 0 0 0 12 7.5z"
            />
          </svg>
        </a>

        <!-- Lien LinkedIn -->
        <a
          href="https://www.linkedin.com/in/julesdupaquier"
          target="_blank"
          rel="noopener noreferrer"
          aria-label="LinkedIn"
          class="text-blanc hover:text-green transition-colors"
        >
          <svg
            xmlns="http://www.w3.org/2000/svg"
            viewBox="0 0 448 512"
            fill="currentColor"
            class="w-6 h-6"
          >
            <path
              d="M100.28,448H7V148H100ZM53.79,108C24,108,0,83.77,0,54A53.79,53.79,0,1,1,107.58,54C107.58,83.77,83.56,108,53.79,108ZM447,448H354V302c0-34.7-.7-79.26-48.26-79.26-48.31,0-55.72,37.72-55.72,76.73V448H157V148h93v41h1c12.93-24,44.52-48,91.65-48C439,141,447,194,447,259Z"
            />
          </svg>
        </a>
      </div>

      <!-- Texte principal -->
      <p class="text-disabled text-sm mt-6">
        &copy; {{ currentYear }} CybGuard - Tous droits réservés.
      </p>
    </div>
  </footer>
</template>

<script setup>
// Obtenir l'année actuelle dynamiquement
const currentYear = new Date().getFullYear();
</script>

