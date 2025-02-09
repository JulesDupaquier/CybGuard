<template>
  <header
    class="bg-gradient-to-b from-noir to-transparent fixed top-0 left-0 w-full z-50 py-6 px-8 flex justify-between items-center"
  >
    <!-- Logo -->
    <NuxtLink href="/">
      <Logo />
    </NuxtLink>

    <!-- Menu Desktop -->
    <nav class="hidden md:flex items-center space-x-8">
      <NuxtLink href="/protection" class="hover:text-green">Protection</NuxtLink>
      <NuxtLink href="/mentions-legales" class="hover:text-green">Mentions Légales</NuxtLink>
      
      <!-- Bouton Télécharger l'App -->
      <NuxtLink to="/download" class="btn btn-header flex items-center">
        <svg
          xmlns="http://www.w3.org/2000/svg"
          class="w-5 h-5 mr-2"
          fill="none"
          viewBox="0 0 24 24"
          stroke="currentColor"
          stroke-width="2"
        >
          <path
            stroke-linecap="round"
            stroke-linejoin="round"
            d="M12 4v12m0 0l-4-4m4 4l4-4m-4 4V4m0 16h8m-8 0H4"
          />
        </svg>
        Télécharger l'App
      </NuxtLink>
    </nav>

    <!-- Menu Mobile -->
    <div class="md:hidden">
      <!-- Bouton Menu Burger -->
      <button @click="toggleMenu" class="focus:outline-none text-blanc">
        <!-- Icône menu burger -->
        <svg
          xmlns="http://www.w3.org/2000/svg"
          class="w-8 h-8"
          fill="none"
          viewBox="0 0 24 24"
          stroke="currentColor"
          stroke-width="2"
        >
          <path
            stroke-linecap="round"
            stroke-linejoin="round"
            d="M3 6h18M3 12h18M3 18h18" 
          />
        </svg>
      </button>
    </div>

    <!-- Overlay (assombrissement de la page) -->
    <div
      v-if="isMenuOpen"
      @click.self.prevent.stop="closeMenu"
      class="
        fixed inset-0 bg-black bg-opacity-50 z-[49]
        transition-opacity duration-300 ease-in-out md:hidden
      "
    ></div>

    <!-- Menu Ouvrant Mobile -->
    <div
      :class="{ 'translate-x-full': !isMenuOpen, 'translate-x-0': isMenuOpen }"
      class="
        fixed top-0 right-0 w-[70%] h-full bg-noir shadow-lg z-[50]
        flex flex-col justify-center items-center py-8 px-6 space-y-6
        transform transition-transform duration-300 ease-in-out md:hidden
      "
    >
      <!-- Bouton Fermer -->
      <button @click="closeMenu" class="absolute top-6 right-6 text-blanc">
        <!-- Icône "fermer" -->
        <svg
          xmlns="http://www.w3.org/2000/svg"
          class="w-8 h-8"
          fill="none"
          viewBox="0 0 24 24"
          stroke="currentColor"
          stroke-width="2"
        >
          <path
            stroke-linecap="round"
            stroke-linejoin="round"
            d="M6 18L18 6M6 6l12 12"
          />
        </svg>
      </button>

      <!-- Liens du Menu -->
      <NuxtLink @click.native="closeMenu" href="/protection" class="text-blanc hover:text-green text-xl">
        Protection
      </NuxtLink>
      <NuxtLink @click.native="closeMenu" href="/mentions-legales" class="text-blanc hover:text-green text-xl">
        Mentions Légales
      </NuxtLink>

      <!-- Bouton Télécharger l'App dans le menu mobile -->
      <NuxtLink
        @click.native="closeMenu"
        to="/download"
        class="
          btn btn-header flex items-center
        "
      >
        <svg
          xmlns="http://www.w3.org/2000/svg"
          class="w-5 h-5 mr-2"
          fill="none"
          viewBox="0 0 24 24"
          stroke="currentColor"
          stroke-width="2"
        >
          <path
            stroke-linecap="round"
            stroke-linejoin="round"
            d="M12 4v12m0 0l-4-4m4 4l4-4m-4 4V4m0 16h8m-8 0H4"
          />
        </svg>
        Télécharger l'App
      </NuxtLink>
    </div>
  </header>
</template>

<script setup lang="ts">
import { ref } from "vue";

// État pour ouvrir/fermer le menu mobile
const isMenuOpen = ref(false);

const toggleMenu = () => {
  isMenuOpen.value = !isMenuOpen.value;
};

const closeMenu = () => {
  isMenuOpen.value = false;
};
</script>
