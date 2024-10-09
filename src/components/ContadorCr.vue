<script>
export default {
    name: 'ContadorCr',
    data() {
        return {
            contador: 0,
        };
    },
};
</script>

<template>
    <div>
        <input type="number" v-model="contador" />
        <p>El número ingresado es: {{ contador }}</p>
    </div>
</template>

<style scoped></style>
