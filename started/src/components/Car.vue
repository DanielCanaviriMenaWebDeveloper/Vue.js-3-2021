<template>
    <div>
        <h2>Componente Car</h2>
        <p>Marca: {{ brand }}</p>
        <p>Modelo: {{ model }}</p>
        <p>Color: {{ color[1] }}</p>
        <p>Precio: {{ price }} $</p>
        <p>Potencia: {{ power }} CV</p>
        <p>{{ mensaje.title }}</p>
        <p>{{ mensaje.text }}</p> 
        <Test />
    </div>
</template>

<script>
import Test from './Test';
export default {
    /* data() {
        return {
            brand: "Toyota",
            model: 2021,
            color: ['Negro', 'Verde', 'Azul'],
            price: 5000,
            power: 180,
            mensaje: {
                title: 'Titulo del mensaje',
                text: 'Texto del mensaje'
            },
        }
    }, */
    setup() {
        const brand = "Nissan";
        const model = 2020;
        const color = ['Negro', 'Rojo', 'Verde'];
        const price = 6000;
        const power = 340;
        const mensaje = { 
            title: 'Titulo del mensaje',
            text: 'Texto del mensaje'
        };

        return {
            brand, model, color, price, power, mensaje
        };
    },
    components: {
        Test,
    },
};
</script>

<style>

</style>