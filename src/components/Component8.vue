<!-- 8.-  Clases dinámicas con v-bind:class
Enunciado: Crea un componente que tenga un botón. El botón debe tener una clase CSS dinámica que cambie según un valor booleano en el data. Usa v-bind:class para aplicar la clase condicionalmente. -->

<template>
    <div class="button-container">
      <h2>Clases Dinámicas con v-bind:class</h2>
      <button 
        :class="buttonClass" 
        @click="toggleActive"
      >
        {{ isActive ? 'Activo' : 'Inactivo' }}
      </button>
    </div>
  </template>
  
  <script setup>
  import { ref, computed } from 'vue';
  
  const isActive = ref(false);
  
  function toggleActive() {
    isActive.value = !isActive.value; 
  }
  
  const buttonClass = computed(() => ({
    active: isActive.value, 
    inactive: !isActive.value,
  }));
  </script>
  
  <style scoped>
  .button-container {
    text-align: center; 
    margin-top: 20px;
  }
  
  button {
    padding: 10px 15px; 
    border: none; 
    border-radius: 5px; 
    font-size: 16px; 
    cursor: pointer; 
    transition: background-color 0.3s; 
  }
  
  .active {
    background-color: #47ad4c;
    color: white;
  }
  
  .inactive {
    background-color: #fc2a2a; 
    color: white; 
  }
  </style>
  