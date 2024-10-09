<!-- 6.-  Enlace dinámico al atributo href de un enlace
Enunciado: Crea un componente que tenga un enlace (a) donde el href sea dinámico. 
El valor del enlace debe estar en el data del componente y cambiarse mediante v-bind. -->

<template>
  <div>
    <!-- <a :href="link" target="_blank">Enlace dinámico</a> -->
    <select v-model="selectedLink">
      <option value="" disabled>Selecciona un enlace</option>
      <option v-for="link in link" :value="link">{{ link }}</option>
    </select>
    <p>
      <a :href="selectedLink" target="_blank">Enlace dinámico</a>
    </p>
  </div>
</template>

<script>
export default {
  name: "Component6",
  data() {
    return {
      link: ["https://www.google.com", "https://www.youtube.com"],
      selectedLink: "",
    };
  },
};
</script>

<style scoped>
div {
  padding-bottom: 20px;
}
</style>
