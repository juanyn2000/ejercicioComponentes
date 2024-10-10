<!-- 7.-  Enlace dinámico al atributo src de una imagen -->
<!-- Enunciado: Crea un componente que muestre una imagen con un src dinámico. El enlace de la imagen debe estar almacenado en el data del componente y cambiarse mediante v-bind. -->

<template>
    <div class="image-container">
      <h2>Enlace dinámico al atributo src de una imagen</h2>
      <button class="change-image-button" @click="changeImage">Cambiar Imagen</button>
      <img :src="currentImage" alt="Imagen Dinámica" class="dynamic-image" />
    </div>
  </template>
  
  <script setup>
  import { ref } from 'vue';
  
  const images = [
    new URL('../assets/gato.png', import.meta.url).href,
    new URL('../assets/perro.png', import.meta.url).href,
  ];
  
  const currentImage = ref(images[0]); 
  
  function changeImage() {
    currentImage.value = currentImage.value === images[0] ? images[1] : images[0]; 
  }
  </script>
  
  <style scoped>
  .image-container {
    text-align: center; 
    background-color: white; 
    padding: 20px; 
    border-radius: 10px; 
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1); 
    max-width: 400px; 
    margin: auto;
  }
  
  .change-image-button {
    margin-bottom: 10px; 
    padding: 10px 15px;
    background-color: #42b883; 
    color: white;
    border: none;
    border-radius: 5px; 
    cursor: pointer; 
    font-size: 16px; 
  }
  
  .change-image-button:hover {
    background-color: #36a76a; 
  }
  
  .dynamic-image {
    width: 300px;
    height: auto; 
    border: 2px solid #ccc;
    border-radius: 10px; 
    margin-top: 10px; 
  }
  </style>
  