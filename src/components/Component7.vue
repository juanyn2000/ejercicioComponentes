<!-- 7.-  Enlace dinámico al atributo src de una imagen
Enunciado: Crea un componente que muestre una imagen con un src dinámico. 
El enlace de la imagen debe estar almacenado en el data del componente y cambiarse mediante v-bind. -->
<template>
  <div>
    <img :src="imgURl" alt="imagen dinámica" />
  </div>
</template>

<script>
export default {
  name: "Component7",
  data() {
    return {
      imgURl:
        "https://arc-anglerfish-arc2-prod-copesa.s3.amazonaws.com/public/3R4GI4FZVFDK5N3QBBTCDVIX7Q.jpg",
    };
  },
};
</script>

<style scoped>
img {
  width: 400px;
}
</style>
