<!-- src/components/Home.vue -->
<template>
    <div>
      <h1>Welcome to Our Cafe!</h1>
      <button @click="goToMenu">See Our Menu</button>
    </div>
  </template>
  
  <script setup>
  import { useRouter } from 'vue-router'
  
  const router = useRouter()
  
  const goToMenu = () => {
    router.push('/menu')
  }
  </script>
  