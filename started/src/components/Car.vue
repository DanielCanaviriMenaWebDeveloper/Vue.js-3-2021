<template>
    <div>
        <h2>Componente Car</h2>
        <p>Marca: {{ brand }}</p>
        <p>Modelo: {{ model }}</p>
        <p>Color: {{ colors[1] }}</p>
        <p>Precio: {{ price }} $</p>
        <p>Potencia: {{ power }} CV</p>
        <p>{{ mensaje.title }}</p>
        <p>{{ mensaje.text }}</p>
        <!-- Ejemplo del uso de la directiva v-for --> 
        <ul>Lista de Colores:
            <li v-for="(color, index) in colors" :key="index">
                {{ index }} : {{ color }}
            </li>
        </ul>
        <!-- <ul>Lista de Potencias:
            <li v-for="(potencia, index) in potencias" :key="index">
                <template v-if="potencia<=120">{{ potencia }}</template>
            </li>
        </ul> -->
        <ul>
            <template v-for="(potencia, index) in potencias" :key="index"><!-- No es recomendable definir una key en un elemento inexistente -->
                <li v-if="potencia < 300">{{ potencia }}</li>
            </template>
        </ul>

        <ul v-for="(tecnologia, index) in tecnologias" :key="index">
            <li>{{ tecnologia }}</li>
        </ul>
        
        <p>Potencias menores a 280:</p>
        <ul v-for="(potencia, index) in potencias" :key="index"> 
            <li v-if="potencia < 280">Urbana : {{ potencia }}</li>
            <li v-else-if="potencia === 280">Hibrido : {{ potencia }}</li>
            <li v-else>Carrera : {{ potencia }}</li>
            
            <li v-if="potencia < 700">2do Recorrido : {{ potencia }}</li>

            <li v-if="potencia < 150">3er Recorrido : {{ potencia }}</li>
        </ul>
        <Test />
    </div>
</template>

<script>
import Test from './Test';
export default {
    /* Option API */
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
    /* Composition API */
    setup() {
        const brand = "Nissan";
        const model = 2020;
        const colors = ['Negro', 'Rojo', 'Verde', 'Azul', 'Morado', 'Rosado'];
        const price = 6000;
        const power = 340;
        const mensaje = { 
            title: 'Titulo del mensaje',
            text: 'Texto del mensaje'
        };
        const potencias = [60, 80, 350, 120, 450, 160, 200, 280, 300, 390, 540, 500];
        const tecnologias = ['JS', 'CSS', 'HTML', 'JQuery', 'React', 'PHP', 'Vue.js', 'Angular'];
        return {
            brand, model, colors, price, power, mensaje, potencias, tecnologias
        };
    },
    components: {
        Test,
    },
};
</script>

<style>

</style>