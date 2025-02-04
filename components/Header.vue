<template>
  <header class="bg-transparent sticky top-0 mx-auto h-8 py-12 px-12 flex justify-between items-center">
    <a href="/home"><CybGuardLogo/></a>
    <div class="hidden md:flex space-x-8">
      <a href="#" class="text-blanc hover:text-bleu">Features</a>
      <a href="#" class="text-blanc hover:text-bleu">Pricing</a>
      <a href="#" class="text-blanc hover:text-bleu">Contact</a>
    </div>
    <div class="md:hidden">
      <button class="focus:outline-none">
        <svg
          class="w-6 h-6"
          fill="none"
          stroke="currentColor"
          viewBox="0 0 24 24"
        >
          <path
            stroke-linecap="round"
            stroke-linejoin="round"
            stroke-width="2"
            d="M4 6h16M4 12h16m-7 6h7"
          ></path>
        </svg>
      </button>
    </div>
  </header>
</template>
