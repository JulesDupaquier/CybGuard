<template>
  <main
    class="background-image min-h-screen flex justify-center items-center bg-cover bg-center"
  >
    <div
      class="bg-white bg-opacity-75 p-8 rounded-lg shadow-lg w-full max-w-lg sm:w-full sm:max-w-xs"
    >
      <!-- Logo -->
      <div class="flex justify-center mb-6">
        <PauseCoffee class="h-12" />
      </div>

      <h2 class="text-2xl font-semibold text-center mb-6 text-[#D14646]">
        Gagnez 1 an de café gratuit !
      </h2>
      <p class="text-sm text-center mb-6 text-gray-600">
        Tentez de remporter 1 an de café ! Veuillez remplir les champs ci-dessous pour nous transmettre vos
        informations. Ces données sont essentielles pour continuer votre inscription.
      </p>

      <!-- Formulaire -->
      <form @submit.prevent="submitForm">
        <div class="mb-4">
          <label
            for="firstName"
            class="block text-sm font-medium text-[#003D44]"
            >Prénom</label
          >
          <input
            type="text"
            id="firstName"
            v-model="firstName"
            class="mt-1 block w-full px-4 py-2 border border-[#003D44] rounded-md shadow-sm focus:outline-none focus:ring-2 focus:ring-[#003D44]"
            required
          />
        </div>
        <div class="mb-4">
          <label for="lastName" class="block text-sm font-medium text-[#003D44]"
            >Nom</label
          >
          <input
            type="text"
            id="lastName"
            v-model="lastName"
            class="mt-1 block w-full px-4 py-2 border border-[#003D44] rounded-md shadow-sm focus:outline-none focus:ring-2 focus:ring-[#003D44]"
            required
          />
        </div>
        <div class="mb-6">
          <label for="email" class="block text-sm font-medium text-[#003D44]"
            >Email</label
          >
          <input
            type="email"
            id="email"
            v-model="email"
            class="mt-1 block w-full px-4 py-2 border border-[#003D44] rounded-md shadow-sm focus:outline-none focus:ring-2 focus:ring-[#003D44]"
            required
          />
        </div>
        <div class="flex justify-center">
          <button
            type="submit"
            class="px-6 py-3 bg-[#003D44] text-white font-semibold rounded-lg hover:bg-[#005C64] focus:outline-none focus:ring-2 focus:ring-[#003D44]"
          >
            Envoyer
          </button>
        </div>
      </form>
    </div>
  </main>
</template>

<script>
export default {
  data() {
    return {
      firstName: "",
      lastName: "",
      email: "",
    };
  },
  methods: {
    submitForm() {
      // Traitez ici les données du formulaire
      console.log("Form submitted", this.firstName, this.lastName, this.email);
      this.$router.push("/landing"); // Redirection vers la landing page
    },
  },
};
</script>

<style scoped>

.background-image {
  background-image: url('/public/img/background-maxicoffe.jpg');
  background-position: center;
  background-size: cover;
}

@media (max-width: 640px) {
  .sm\:w-full {
    width: 100%;
  }
  .sm\:max-w-xs {
    max-width: 100%;
  }
}
</style>
