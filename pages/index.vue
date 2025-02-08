<template>
  <Header />

  <!-- Section Vidéo -->
  <section class="relative w-full h-screen">
    <video
      class="absolute inset-0 w-full h-full object-cover"
      autoplay
      muted
      loop
      playsinline
    >
      <source src="/video/Background_Video_CybGuard.mp4" type="video/mp4" />
      Your browser does not support the video tag.
    </video>

    <div class="absolute inset-0 flex flex-col justify-center items-center text-center z-20">
      <h1>
        <span class="text-negative">Attention</span>, vous auriez pu exposer vos données au monde entier.
      </h1>
      <p>
        CybGuard peut vous aider à sécuriser vos données.
      </p>
      <div class="space-x-4">
        <button>Découvrez CybGuard</button>
        <NuxtLink to="/download">
          <button>Téléchargez l'application</button>
        </NuxtLink>
      </div>
    </div>

    <!-- Icône Flèche -->
    <div class="absolute bottom-8 left-1/2 transform -translate-x-1/2 z-30">
      <a href="#features"
        class="flex items-center justify-center w-12 h-12 border-blue border rounded-full hover:bg-blue hover:text-noir transition duration-300 animate-bounce"
        aria-label="Descendre à la section suivante"
      >
        <svg xmlns="http://www.w3.org/2000/svg" class="w-full h-full" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
          <path stroke-linecap="round" stroke-linejoin="round" d="M19 9l-7 7l-7 -7" />
        </svg>
      </a>
    </div>
  </section>

  <!-- Section Fonctionnalités -->
  <section id="features" class="py-16">
    <div class="container mx-auto px-6 text-center">
      <h2>Pourquoi choisir CybGuard ?</h2>
      <p>Découvrez comment CybGuard peut protéger vos données et vous aider à adopter de bonnes pratiques en cybersécurité.</p>

      <!-- Grille des fonctionnalités -->
      <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-y-8 gap-x-6">
        <!-- Fonctionnalité -->
        <div class="bg-noir25 p-[20px] rounded-lg shadow-md">
          <h3>🔑 Gestionnaire de mots de passe</h3>
          <p>Générez, stockez et gérez vos mots de passe en toute sécurité.</p>
        </div>

        <!-- Autres fonctionnalités... -->
      </div>
    </div>
  </section>

  <!-- Section Avis -->
  <section id="avis" class="place-items-center py-[60px]">
    <h2>Des utilisateurs en rêvent</h2>
    <AvisCarousel />
    <NuxtLink to="/feedback-form">
      <button>Donnez votre avis !</button>
    </NuxtLink>
  </section>

  <!-- Footer -->
  <Footer />
</template>
