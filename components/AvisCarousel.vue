<script>
import { ref, onMounted, onUnmounted } from "vue";

export default {
  setup() {
    const currentIndex = ref(0);
    const reviews = ref([
      {
        name: "Benoît F.",
        work: 'Étudiant Salarié',
        image: "/img/Profile-Picture.webp",
        feedback: "Essentiel pour prendre conscience des dangers de la cybersécurité",
      },
      {
        name: "Lucas C.",
        work: "Étudiant",
        image: "/img/Profile-Picture.webp",
        feedback: "Super initiative pour sensibiliser et éviter les piratages",
      },
      {
        name: "Sophie Martin",
        work: "Étudiant Salarié",
        image: "/img/Profile-Picture.webp",
        feedback:
          "Je recommande fortement, la sécurité en ligne est essentielle !",
      },
    ]);

    const containerRef = ref(null);
    let startX = 0;
    let isDragging = false;

    const prevSlide = () => {
      currentIndex.value =
        (currentIndex.value - 1 + reviews.value.length) % reviews.value.length;
    };

    const nextSlide = () => {
      currentIndex.value = (currentIndex.value + 1) % reviews.value.length;
    };

    const onTouchStart = (e) => {
      startX = e.touches[0].clientX;
      isDragging = true;
    };

    const onTouchMove = (e) => {
      if (!isDragging) return;
      const currentX = e.touches[0].clientX;
      const diff = startX - currentX;
      if (Math.abs(diff) > 50) {
        if (diff > 0) {
          nextSlide();
        } else {
          prevSlide();
        }
        isDragging = false;
      }
    };

    const onTouchEnd = () => {
      isDragging = false;
    };

    onMounted(() => {
      const container = containerRef.value;
      if (container) {
        container.addEventListener('touchstart', onTouchStart);
        container.addEventListener('touchmove', onTouchMove);
        container.addEventListener('touchend', onTouchEnd);
      }
    });

    onUnmounted(() => {
      const container = containerRef.value;
      if (container) {
        container.removeEventListener('touchstart', onTouchStart);
        container.removeEventListener('touchmove', onTouchMove);
        container.removeEventListener('touchend', onTouchEnd);
      }
    });

    return { currentIndex, reviews, prevSlide, nextSlide, containerRef };
  },
};
</script>

<template>
  <div class="w-full max-w-4xl mx-auto py-10 overflow-hidden relative" ref="containerRef">
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
        <h4 class="text-blanc">{{ review.name }}</h4>
        <h7 class="text-disabled">{{ review.work }}</h7>
        <p class="mt-4">"{{ review.feedback }}"</p>
      </div>
    </div>
    <div
      class="absolute top-1/2 left-0 transform -translate-y-1/2 p-2 cursor-pointer text-blanc"
      @click="prevSlide"
    >
      <
    </div>
    <div
      class="absolute top-1/2 right-0 transform -translate-y-1/2 p-2 cursor-pointer text-blanc"
      @click="nextSlide"
    >
      >
    </div>
  </div>
</template>

<style scoped>
.transition-transform {
  display: flex;
  width: 100%;
  touch-action: pan-y;
}
</style>
