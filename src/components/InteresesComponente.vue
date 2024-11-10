<script setup>
import { ref } from 'vue';

//Este es un arreglo con ref para que se pueda reactivar el cambio de los intereses
const intereses = ref([
    'Desarrollo de Software de Código Abierto: Hasta ahora contribuyo proyectos en GitHub de Golang Latam, colaborando con otros desarrolladores para mejorar herramientas y librerías populares.',
    'Deportes al Aire Libre: Me gusta hacer caminatas en mi pueblo junto con amigos, lo que me ayuda a mantenerme en forma y aclarar mi mente.',
    'Tecnología de Innovación: Me apasiona explorar nuevas tendencias tecnológicas como tecnología en la nube, go, angular, vue, etc.',
    "Dibujo: Me gusta dibujar en mi tiempo libre, lo que me ayuda a relajarme y a ser más creativo.",
    "Instrumentos Musicales: Toco el bajo eléctrico, es un hobby que me ayuda a despejarme y a disfrutar de la música."    
]);
</script>

<template>
    <div class="intereses-contenedor">
        
        <ul class="contenedor-lista">
            <li class="item" v-for="interes in intereses" :key="interes">
                {{ interes }}
            </li>
        </ul>
    </div>
</template>

<style scoped>
.intereses-contenedor {
    background-color: #021526;
    display: flex;
    position: relative;
    margin: 0 auto;
    max-width: 85%;
    padding: 1rem;
}

.contenedor-lista {
    list-style-type: none;
    padding: 1rem;
    margin-bottom: .5rem;
    color: var(--vt-c-white-soft);
    font-size: 1.4rem;
    text-shadow: 3px 3px 6px rgba(0, 0, 0, 1);
}

.item {
    margin-bottom: 1rem;
}
</style>