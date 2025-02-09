<script>
import { ref, onMounted, onUnmounted } from "vue";

export default {
  setup() {
    const currentIndex = ref(0);
    const reviews = ref([
      {
        name: "Benoît F.",
        work: "Étudiant Salarié",
        image: "/img/Profile-Picture.webp",
        feedback: "Essentiel pour prendre conscience des dangers de la cybersécurité",
      },
      {
        name: "Jaël A.",
        work: "Étudiante",
        image: "/img/Profile-Picture.webp",
        feedback:
          "Un bon outil de sensibilisation aux pièges en ligne.",
      },
      {
        name: "Lucas C.",
        work: "Étudiant",
        image: "/img/Profile-Picture.webp",
        feedback: "Super initiative pour sensibiliser et éviter les piratages",
      },
      {
        name: "Faris H.",
        work: "Étudiant Salarié",
        image: "/img/Profile-Picture.webp",
        feedback: "Une appli superbe pour ce sentir en toute sécurité.",
      },
      {
        name: "Estelle C.",
        work: "Étudiante",
        image: "/img/Profile-Picture.webp",
        feedback: "C'est important pour ceux qui ne savent pas comment se protéger !",
      },
      {
        name: "Anonyme",
        work: "Étudiant",
        image: "/img/Profile-Picture.webp",
        feedback: "Une appli qui apprend la vraie valeur de nos données personnelles.",
      },

    ]);

    const containerRef = ref(null);

    const prevSlide = () => {
      currentIndex.value =
        (currentIndex.value - 1 + reviews.value.length) % reviews.value.length;
    };

    const nextSlide = () => {
      currentIndex.value = (currentIndex.value + 1) % reviews.value.length;
    };

    // Scroll horizontal avec la molette
    const onWheelScroll = (e) => {
      e.preventDefault();
      if (e.deltaY > 0) nextSlide();
      else prevSlide();
    };

    // Gestion du swipe tactile
    let startX = 0;
    let isDragging = false;

    const onTouchStart = (e) => {
      startX = e.touches[0].clientX;
      isDragging = true;
    };

    const onTouchMove = (e) => {
      if (!isDragging) return;
      const currentX = e.touches[0].clientX;
      const diff = startX - currentX;
      if (Math.abs(diff) > 50) {
        if (diff > 0) nextSlide();
        else prevSlide();
        isDragging = false;
      }
    };

    const onTouchEnd = () => {
      isDragging = false;
    };

    // Ajout des événements
    onMounted(() => {
      const container = containerRef.value;
      if (container) {
        container.addEventListener("touchstart", onTouchStart);
        container.addEventListener("touchmove", onTouchMove);
        container.addEventListener("touchend", onTouchEnd);
        container.addEventListener("wheel", onWheelScroll, { passive: false });
      }
    });

    // Suppression des événements
    onUnmounted(() => {
      const container = containerRef.value;
      if (container) {
        container.removeEventListener("touchstart", onTouchStart);
        container.removeEventListener("touchmove", onTouchMove);
        container.removeEventListener("touchend", onTouchEnd);
        container.removeEventListener("wheel", onWheelScroll);
      }
    });

    return { currentIndex, reviews, prevSlide, nextSlide, containerRef };
  },
};
</script>

<template>
  <div class="w-full max-w-4xl mx-auto py-10 overflow-hidden relative" ref="containerRef">
    <!-- Carrousel -->
    <div
      class="flex transition-transform duration-500 ease-in-out"
      :style="{ transform: `translateX(-${currentIndex * 100}%)` }"
    >
      <div
        v-for="(review, index) in reviews"
        :key="index"
        class="w-full flex-shrink-0 p-6 bg-noir25 shadow-lg rounded-2xl text-center"
      >
        <img
          :src="review.image"
          alt="Photo de profil"
          class="w-16 h-16 rounded-full mb-4 mx-auto"
        />
        <h4 class="text-vert">{{ review.name }}</h4>
        <h7 class="text-disabled">{{ review.work }}</h7>
        <p class="mt-4">"{{ review.feedback }}"</p>
      </div>
    </div>

    <!-- Flèche gauche -->
    <div
      class="absolute top-1/2 left-4 transform -translate-y-1/2 p-2 cursor-pointer text-blanc bg-noir25 border border-vert rounded-full hover:bg-vert transition-all duration-300"
      @click="prevSlide"
    >
      <svg
        xmlns="http://www.w3.org/2000/svg"
        fill="none"
        viewBox="0 0 24 24"
        stroke-width="2"
        stroke="currentColor"
        class="w-6 h-6"
      >
        <path stroke-linecap="round" stroke-linejoin="round" d="M15 19l-7-7 7-7" />
      </svg>
    </div>

    <!-- Flèche droite -->
    <div
      class="absolute top-1/2 right-4 transform -translate-y-1/2 p-2 cursor-pointer text-blanc bg-noir25 border border-vert rounded-full hover:bg-vert transition-all duration-300"
      @click="nextSlide"
    >
      <svg
        xmlns="http://www.w3.org/2000/svg"
        fill="none"
        viewBox="0 0 24 24"
        stroke-width="2"
        stroke="currentColor"
        class="w-6 h-6"
      >
        <path stroke-linecap="round" stroke-linejoin="round" d="M9 5l7 7-7 7" />
      </svg>
    </div>
  </div>
</template>

<style scoped>
.transition-transform {
  display: flex;
  width: 100%;
  touch-action: pan-y; /* Permet le swipe tactile */
}
</style>
