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

    <!-- Superposition avec dégradé -->
    <div
      class="absolute inset-0 bg-gradient-to-b from-transparent to-noir z-10"
    ></div>

    <!-- Contenu principal -->
    <div
      class="absolute inset-0 flex flex-col justify-center items-center text-center z-20 px-4"
    >
      <!-- Titre principal -->
      <h1
        class="text-xl sm:text-2xl md:text-4xl lg:text-5xl font-bold text-blanc leading-tight max-w-4xl mx-auto"
      >
        <span class="text-negative">Et si c'était un piège ?</span> Vos données
        auraient pu être entre de mauvaises mains.
      </h1>

      <!-- Paragraphe -->
      <p
        class="mt-4 text-sm sm:text-base md:text-lg lg:text-xl text-blanc max-w-2xl"
      >
        Pas de panique ! Ce n'était qu'un projet étudiant. Mais dans la réalité,
        les menaces sont bien réelles. CybGuard vous aide à protéger vos données
        et à adopter de bonnes pratiques en cybersécurité.
      </p>

      <!-- Boutons -->
      <div class="mt-6 flex flex-wrap justify-center gap-4">
        <button class="btn btn-primary">Découvrez CybGuard</button>
        <NuxtLink to="/waitlist">
          <button class="btn btn-secondary">S'inscrire à la liste d'attente</button>
        </NuxtLink>
      </div>
    </div>

<!-- Icône Flèche -->
<div class="absolute bottom-8 left-1/2 transform -translate-x-1/2 z-30">
  <a
    href="#about"
    class="menu-icon border-2 border-green rounded-full p-2 animate-bounce"
    aria-label="Descendre à la section suivante"
  >
    <svg
      xmlns="http://www.w3.org/2000/svg"
      class="w-6 h-6 text-green"
      viewBox="0 0 24 24"
      fill="none"
      stroke="currentColor"
      stroke-width="2"
    >
      <path stroke-linecap="round" stroke-linejoin="round" d="M19 9l-7 7l-7 -7" />
    </svg>
  </a>
</div>

  </section>

  <!-- Section About Jules -->
  <section id="about" class="py-16 bg-noir">
    <div class="container mx-auto px-6 flex flex-col md:flex-row items-center">
      <!-- Texte explicatif à gauche -->
      <div class="w-full md:w-1/2 text-center md:text-left mb-8 md:mb-0">
        <h2 class="text-2xl font-bold text-blanc mb-4">
          Pas de panique ! Ce n'est que moi.
        </h2>
        <p class="text-lg text-blanc leading-relaxed text-justify">
          Je suis <strong>Jules Dupaquier</strong>, étudiant en BUT MMI 3 et créateur du projet
          <strong>CybGuard</strong>. Ce projet a été conçu pour sensibiliser les utilisateurs aux
          dangers du quishing et d'autres cyberattaques. Mon objectif est de
          fournir un projet clé basé sur l'éveil à la cybersécurité et responsabilité numérique.
        </p>
      </div>

      <!-- Image à droite -->
      <div class="w-full md:w-1/2">
        <JulesDupaquier />
      </div>
    </div>
  </section>

  <!-- Section About Quishing -->
  <section id="quishing" class="py-16">
    <div class="container mx-auto px-6 flex flex-col md:flex-row items-center">
      <!-- Infographie (Quishing.vue) à gauche -->
      <div class="w-full md:w-1/2 mb-8 md:mb-0">
        <Quishing />
      </div>

      <!-- Texte explicatif à droite -->
      <div class="w-full md:w-1/2 text-center md:text-left">
        <h2 class="text-2xl font-bold text-blanc mb-4">
          Le Quishing ?
        </h2>
        <p class="text-lg text-blanc leading-relaxed text-justify">
          Le <strong>quishing</strong>, ou hameçonnage par QR Code, est une
          méthode de cyberattaque en pleine expansion. Les cybercriminels
          exploitent la popularité des QR Codes pour tromper les utilisateurs,
          en les redirigeant vers des sites frauduleux ou en installant des
          logiciels malveillants sur leurs appareils. Ces QR Codes malveillants
          sont souvent placés dans des lieux publics, envoyés par email ou
          intégrés dans des publicités.
        </p>
      </div>
    </div>
  </section>

  <!-- Section Fonctionnalités -->
  <section id="features" class="py-16 bg-noir text-center">
    <!-- Titre de la section -->
    <h2
      class="text-xl sm:text-2xl md:text-3xl lg:text-4xl font-bold mb-6 text-blanc"
    >
      Pourquoi choisir CybGuard ?
    </h2>

    <!-- Description de la section -->
    <p
      class="text-sm sm:text-base md:text-lg lg:text-xl mb-12 max-w-xl mx-auto text-blanc"
    >
      Découvrez comment CybGuard peut protéger vos données et vous aider à
      adopter de bonnes pratiques en cybersécurité.
    </p>

    <!-- Grille des fonctionnalités -->
    <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-y-8 gap-x-6">
      <!-- Fonctionnalité : Gestionnaire de mots de passe -->
      <div class="card">
        <span class="text-blanc text-[40px]">🔑</span>
        <h3>Gestionnaire de mots de passe</h3>
        <p>Générez, stockez et gérez vos mots de passe en toute sécurité.</p>
      </div>

      <!-- Fonctionnalité : Protection anti-phishing -->
      <div class="card">
        <span class="text-blanc text-[40px]">🛡️</span>
        <h3>Protection anti-phishing</h3>
        <p>
          Détectez et évitez les tentatives de phishing avant qu'il ne soit trop
          tard.
        </p>
      </div>

      <!-- Fonctionnalité : Alertes en temps réel -->
      <div class="card">
        <span class="text-blanc text-[40px]">📢</span>
        <h3>Alertes en temps réel</h3>
        <p>
          Recevez des notifications instantanées sur les menaces potentielles.
        </p>
      </div>

      <!-- Fonctionnalité : Conseils personnalisés -->
      <div class="card">
        <span class="text-blanc text-[40px]">📚</span>
        <h3>Conseils personnalisés</h3>
        <p>
          Adoptez les meilleures pratiques grâce à des recommandations adaptées.
        </p>
      </div>

      <!-- Fonctionnalité : Simulations interactives -->
      <div class="card">
        <span class="text-blanc text-[40px]">👥</span>
        <h3>Simulations interactives</h3>
        <p>Testez vos connaissances avec des scénarios réalistes.</p>
      </div>

      <!-- Fonctionnalité : Challenges et récompenses -->
      <div class="card">
        <span class="text-blanc text-[40px]">🏆</span>
        <h3>Challenges et récompenses</h3>
        <p>Progressez tout en vous amusant grâce à des défis motivants.</p>
      </div>
    </div>
  </section>

  <!-- Section Avis -->
  <section id="avis" class="py-[60px] bg-noir text-center">
    <!-- Titre de la section -->
    <h2
      class="text-xl sm:text-2xl md:text-3xl lg:text-4xl font-bold mb-6 text-blanc"
    >
      Des étudiants en parlent
    </h2>

    <!-- Carrousel des avis -->
    <AvisCarousel />

    <!-- Lien vers le formulaire d'avis -->
    <NuxtLink to="/feedback-form">
      <button class="btn btn-secondary mt-6">Donnez votre avis !</button>
    </NuxtLink>
  </section>

  <!-- Footer -->
  <Footer />
</template>

<script setup>
// Importation du composant Quishing
import Quishing from "@/components/Quishing.vue";
</script>
