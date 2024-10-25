<script setup>
import pencil from '/src/assets/pencil.svg';
import lista from '/src/assets/lista.svg';
import calendar from '/src/assets/calendar.svg';
import ccv from '/src/assets/cv.svg';
import libro from '/src/assets/libro.svg';

import { ref } from 'vue';

const titulo ='Analista Funcional';
const fecha = 'Desde Diciembre 2023 / Mayo 2024';
const experiencias = ref([
    {id:1, src: pencil, parrafo: 'Definir y Analizar los requerimientos del usuario'},
    {id:2, src: lista, parrafo: 'Analizar y evaluar rendimiento de los sistemas existentes.'},
    {id:3, src: calendar, parrafo: 'Crear planes de cambio basados en los requerimientos analizados.'},
    {id:4, src: ccv, parrafo: 'Comprobar la funcionalidad del producto final.'},
    {id:5, src: libro, parrafo: 'Escribir Manuales de Usuario y Documentacion.'}
])
</script>

<template>
    <div class="card">
        <h3 class="titulo">{{ titulo }}</h3>
        <p class="fecha">{{ fecha }}</p>
        <ul class="item" v-for="experiencia in experiencias" :key="experiencia.id">
            <img class="imagen-svg" :src="experiencia.src" width="45rem" :alt="experiencia.parrafo">
            <p>{{ experiencia.parrafo }}</p>
        </ul>
    </div>
</template>

<style scoped>
.card {
    display: flex;
    flex-direction: column;
    padding: 2rem;
    background-color: #f0dbd7; /* Rosa claro suave */
    border-radius: 15px;
}

.titulo {
    font-size: 1.5rem;
    color: #d1235c; /* Rosa intenso */
}

.fecha {
    font-size: 1rem;
    color: #e24a68; /* Rosa oscuro vibrante */
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
    background-color: #f8c2c1; /* Rosa pastel suave */
    border-radius: 10px;
    color: #d1235c; /* Texto en rosa intenso */
}

h3{
    font-weight: bold;
}
</style>

