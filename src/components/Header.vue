<template>
  <nav
    class="flex text-base flex-wrap items-center justify-between pe-5 pl-10 py-3 md:px-32 md:py-2 bg-black dark:bg-white border-b dark:border-gray-500 dark:text-black text-white"
  >
    <div class="shrink-0">
      <img src="/logo.jpeg" alt="Logo" class="h-10 w-10 rounded-4xl" />
    </div>

    <div class="block md:hidden">
      <button :onclick="toggleMenu" class="p-2 border rounded">Menu</button>
    </div>

    <nav :class="['w-full md:w-auto mt-4 md:mt-0 md:block justify-end', isMenuOpen ? 'flex' : 'hidden']">
      <ul class="flex flex-col text-center item-center md:flex-row space-y-2 md:space-y-0 md:space-x-6 font-medium">
        <li><a href="#" class="hover:text-primary">Accueil</a></li>
        <li><a href="#" class="hover:text-primary">Services</a></li>
        <li><a href="#" class="bg-primary text-white rounded-2xl px-5 py-1">Contact</a></li>
      </ul>
    </nav>
  </nav>
</template>

<script setup lang="ts">
    import { ref } from 'vue';
const isMenuOpen = ref<boolean>(false);

const toggleMenu = (): void => {
    isMenuOpen.value = !isMenuOpen.value;
};
</script>
