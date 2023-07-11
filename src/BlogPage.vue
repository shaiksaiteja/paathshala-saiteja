<template>
    <div :class="{'dark': darkMode}" class="bg-gray-100 dark:bg-gray-800 min-h-screen">
      <nav class="p-4 flex justify-between items-center">
        <h1 class="text-2xl font-bold">My Blog</h1>
        <button @click="toggleDarkMode" class="text-xl" aria-label="Toggle Dark Mode">
          <i v-if="darkMode" class="fas fa-sun"></i>
          <i v-else class="fas fa-moon"></i>
        </button>
      </nav>
  
      <div class="container mx-auto px-4 py-8">
        <div class="grid grid-cols-1 md:grid-cols-3 gap-4">
          <div class="col-span-1">
            <h2 class="text-xl font-bold mb-4">Categories</h2>
            <!-- Render categories here -->
          </div>
  
          <div class="col-span-2">
            <h2 class="text-xl font-bold mb-4">Posts</h2>
            <!-- Render posts here -->
          </div>
        </div>
  
        <div class="mt-8">
          <h2 class="text-xl font-bold mb-4">Comments</h2>
          <!-- Render comments here -->
        </div>
      </div>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        darkMode: false,
      };
    },
    methods: {
      toggleDarkMode() {
        this.darkMode = !this.darkMode;
      },
    },
  };
  </script>
  
  <style scoped>
  /* Add any custom styles or override tailwind classes here */
  </style>
  