<template>
    <header class="fixed top-0 left-0 right-0 z-50 bg-white" :class="{ 'bg-opacity-90 shadow-lg': isScrolled }">
      <nav class="flex items-center justify-between py-3 px-6">
        <div class="flex items-center">
          <h1 class="text-lg font-bold">My Portfolio</h1>
        </div>
        <div class="flex items-center">
          <router-link to="/" class="mx-3 text-gray-600 hover:text-gray-900">Home</router-link>
          <router-link to="/about" class="mx-3 text-gray-600 hover:text-gray-900">About</router-link>
          <router-link to="/contact" class="mx-3 text-gray-600 hover:text-gray-900">Contact</router-link>
        </div>
      </nav>
    </header>
  </template>
  
  <script>
  export default {
    data() {
      return {
        isScrolled: false,
      }
    },
    mounted() {
      window.addEventListener('scroll', this.handleScroll)
    },
    beforeDestroy() {
      window.removeEventListener('scroll', this.handleScroll)
    },
    methods: {
      handleScroll() {
        this.isScrolled = window.scrollY > 50
      },
    },
  }
  </script>
  
  <style scoped>
  header {
    transition: background-color 0.3s, box-shadow 0.3s;
  }
  .bg-opacity-90 {
    background-color: rgba(255, 255, 255, 0.9);
  }
  .shadow-lg {
    box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
  }
  </style>
  