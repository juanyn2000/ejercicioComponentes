<!-- 6.-  Enlace dinámico al atributo href de un enlace
Enunciado: Crea un componente que tenga un enlace (a) donde el href sea dinámico. 
El valor del enlace debe estar en el data del componente y cambiarse mediante v-bind. -->

<template>
    <div>
        <a :href="link" target="_blank">Enlace dinámico</a>
    </div>
</template>

<script>
export default {
  name: "Component6",
  data() {
    return {
      link: 'https://www.google.com',
    };
  },
};
</script>

<style scoped>
</style>
