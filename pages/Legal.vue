<template>
    <div class="min-h-screen bg-noir text-blanc flex flex-col">
      <!-- Header -->
      <Header />
  
      <!-- Section Vidéo -->
      <section class="relative w-full h-[50vh]">
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
        <div class="absolute inset-0 bg-gradient-to-b from-transparent to-noir z-10"></div>
  
        <!-- Titre principal -->
        <div
          class="absolute inset-0 flex flex-col justify-center items-center text-center z-20 px-4"
        >
          <h1 class="text-3xl sm:text-4xl md:text-5xl font-bold text-blanc mb-4">
            Mentions Légales
          </h1>
          <p class="text-lg sm:text-xl max-w-2xl">
            Retrouvez ici toutes les informations légales relatives à CybGuard.
          </p>
        </div>
      </section>
  
      <!-- Contenu principal -->
      <main class="container mx-auto px-6 py-12 space-y-8">
        <!-- Bloc Identité de l'Éditeur -->
        <div class="bg-noir25 p-6 rounded-lg shadow-lg">
          <h2 class="text-vert text-xl font-bold mb-2">Identité de l'Éditeur</h2>
          <p class="text-sm leading-relaxed">
            <span class="text-vert">Nom :</span> Jules Dupaquier<br />
            <span class="text-vert">Adresse :</span> BUT MMI, IUT Nord Franche-Comté, Université Marie et Louis Pasteur - 4 Pl. Tharradin, 25200 Montbéliard<br />
            <span class="text-vert">Email :</span> contact@julesdupaquier.fr
          </p>
        </div>
  
        <!-- Bloc Hébergement -->
        <div class="bg-noir25 p-6 rounded-lg shadow-lg">
          <h2 class="text-vert text-xl font-bold mb-2">Hébergement</h2>
          <p class="text-sm leading-relaxed">
            <span class="text-vert">Nom :</span> Vercel Inc.<br />
            <span class="text-vert">Adresse :</span> 340 S Lemon Ave #4133, Walnut, CA 91789, États-Unis<br />
            <span class="text-vert">Site web :</span>
            <a
              href="https://vercel.com"
              target="_blank"
              rel="noopener noreferrer"
              class="text-blanc hover:text-vert transition-colors"
            >
              https://vercel.com
            </a>
          </p>
        </div>
  
        <!-- Bloc Droits d'Auteur -->
        <div class="bg-noir25 p-6 rounded-lg shadow-lg">
          <h2 class="text-vert text-xl font-bold mb-2">Droits d'Auteur</h2>
          <p class="text-sm leading-relaxed">
            Tous les contenus présents sur ce site (textes, images, vidéos, logos,
            etc.) sont protégés par le droit d'auteur. Toute reproduction,
            distribution ou utilisation non autorisée des contenus est strictement
            interdite sans l'autorisation préalable de Jules Dupaquier.
          </p>
        </div>
  
        <!-- Bloc Limitation de Responsabilité -->
        <div class="bg-noir25 p-6 rounded-lg shadow-lg">
          <h2 class="text-vert text-xl font-bold mb-2">Limitation de Responsabilité</h2>
          <p class="text-sm leading-relaxed">
            Ce site est un projet pédagogique et ne collecte aucune donnée
            personnelle à des fins commerciales. Les informations fournies sur ce
            site sont uniquement à titre informatif et ne constituent pas un
            conseil professionnel. L'éditeur ne saurait être tenu responsable des
            dommages directs ou indirects résultant de l'utilisation du site.
          </p>
        </div>
  
        <!-- Bloc Liens Externes -->
        <div class="bg-noir25 p-6 rounded-lg shadow-lg">
          <h2 class="text-vert text-xl font-bold mb-2">Liens Externes</h2>
          <p class="text-sm leading-relaxed">
            Ce site peut contenir des liens vers des sites externes. L'éditeur ne
            saurait être tenu responsable du contenu ou des pratiques de ces sites
            tiers.
          </p>
        </div>
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
  /* Ajout de styles spécifiques si nécessaire */
  </style>
  