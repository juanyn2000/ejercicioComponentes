<!-- 5.-  Textarea con descripción
Enunciado: Crea un componente que tenga un textarea donde el usuario pueda escribir una descripción. 
Muestra la descripción introducida en tiempo real en un párrafo debajo del textarea. -->
<template>
    <div>
        <textarea v-model="description"></textarea>
        <p>{{ description }}</p>
    </div>
</template>

<script>
export default {
  name: "Component5",
  data() {
    return {
      description: "",
    };
  },
};
</script>