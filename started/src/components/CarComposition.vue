<template>
    <div>
        <h2>Coche - Composition API</h2>
        <p>Marca: {{ brand }}</p>
        <p>Modelo: {{ model }}</p>
    </div>
</template>

<script>
    export default {
        setup() {
            const brand = "Audi";
            const model = "A4";

            return {
                brand,
                model
            };
        },
    };
</script>

<style>

</style>