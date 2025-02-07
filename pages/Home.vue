<script setup lang="ts">
import AvisCarousel from '~/components/AvisCarousel.vue';

</script>

<template>
  <Header />
  <div class="text-white">
    <!-- Section -->
    <section class="container mx-auto max-w-[1000px] py-36 text-center">
      <h1 class="text-5xl text-blanc font-bold mb-6">
        <span class="text-negative">Attention</span>, vous auriez pu exposer vos
        données au monde entier.
      </h1>
      <p class="text-xl text-disabled mb-8">CybGuard peut vous aider à <span class="text-blanc font-bold">sécuriser</span> vos données.</p>
      <div class="space-x-4">
        <button
        >
          Découvrez CybGuard
        </button>
        <button
          class="bg-transparent border border-blanc hover:bg-blanc hover:text-noir text-blanc px-6 py-3 rounded-full"
        >
          Téléchargez l'application
        </button>
      </div>
    </section>
  </div>
  <section>
    <Quishing/>
  </section>
  <section id="avis" class="place-items-center">
    <h2 class="text-center">Des utilisateurs en rêvent</h2>
    <AvisCarousel/>
     <NuxtLink to="https://forms.gle/PPNneoNMbdSdZAPNA"><button>Donnez votre avis !</button></NuxtLink>
  </section>
  <Footer />
</template>
