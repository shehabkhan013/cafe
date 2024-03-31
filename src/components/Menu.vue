<!-- src/components/Menu.vue -->
<template>
    <div class="menu">
      <h1>Menu</h1>
      <ul>
        <li v-for="item in menuItems" :key="item.id" @click="showItemAlert(item.name)">
          {{ item.name }}
        </li>
      </ul>
    </div>
  </template>
  
  
<script setup>
import { toast } from 'vue3-toastify';
import 'vue3-toastify/dist/index.css';


const menuItems = [
  { id: 1, name: 'Coffee' },
  { id: 2, name: 'Tea' },
  { id: 3, name: 'Sandwich' },
  { id: 4, name: 'Barger' }
]

const showItemAlert = (itemName) => {

    toast(`You clicked on ${itemName}`, {
        "theme": "auto",
        "type": "success",
        "dangerouslyHTMLString": true
      }); 
}
</script>