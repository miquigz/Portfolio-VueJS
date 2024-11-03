<script setup>
import { ref } from 'vue';
const titulo = 'Desarrollador Full Stack';
const fecha = 'Desde Abril 2022 / Presente';
const experiencias = ref([
    { id: 1, src: '/src/assets/ventas.svg', parrafo: 'freelance con Angular y firebase, creacion de MVP, gestion de URLs de YT diarias' },
    { id: 2, src: '/src/assets/ecomerce.svg', parrafo: 'Ingreso como becario en finnegans para Desarrollador fullstack con Java y Angular' },
    { id: 3, src: '/src/assets/ecomerce.svg', parrafo: 'Desarrollador fullstack con Angular y Go en finnegans' },
]);
</script>

<template>
    <div class="card">
        <h3 class="titulo">{{ titulo.toLocaleUpperCase() }}</h3>
        <p class="fecha">{{ fecha }}</p>
        <ul class="listado">
            <li class="item" v-for="experencia in experiencias" :key="experencia.id">
                <img class="imagen-svg" :src="experencia.src" width="45rem" :alt="experencia.parrafo">
                <p>{{ experencia.parrafo }}</p>
            </li>
        </ul>
    </div>
</template>

<style scoped>
.card {
    display: flex;
    flex-direction: column;
    padding: 2rem;
    background-color: rgb(28, 41, 52);
    border-radius: 15px;
}

.titulo {
    font-size: 1.5rem;
    color: coral;
}

.fecha {
    font-size: 1rem;
    color: burlywood;
    margin-bottom: 1rem;
}

.listado {
    display: flex;
    flex-direction: column;
}

.item {
    align-items: center;
    display: flex;
    padding: 1rem;
    gap: 1.5rem;
}
</style>