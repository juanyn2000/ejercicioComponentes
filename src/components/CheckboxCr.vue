<script>
export default {
    name: 'CheckboxCr',
    data() {
        return {
            estado: false,
        };
    },
};
</script>

<template>
    <div class="checkbox">
        <div>
            <input type="checkbox" v-model="estado" value="Activo :D" id="estado" />
            <label for="estado">Activo</label>
        </div>
    </div>
    <div v-if="estado">El estado es activo</div>
    <div v-else>El estado es inactivo</div>
</template>

<style scoped></style>
