<script setup>
import { ref } from 'vue';
const fechaColor = ref([
  { color: '#E24A68' }, // Rosa fuerte
  { color: '#D1235C' }, // Rosa intenso
  { color: '#FF5A8A' }, // Rosa vibrante
  { color: '#C2185B' }, // Rosa oscuro intenso
  { color: '#FF3366' }  // Rosa neón
]);


const educacion = ref([
  {fecha: '2024/2025', title: 'Técnicatura Universitaria en Programación', descripcion: 'Incumbencias Profesionales: Operación y programación de computadoras, desarrollo de programas en distintos lenguajes, análisis y control de sistemas informáticos.', enlace:'https://www.youtube.com/'},
  {fecha: '2022/2023', title: 'Desarrollador Full Stack', descripcion: 'Competencias profesionales: Desarrollo de aplicaciones web y móviles utilizando Java para el backend, HTML, CSS, JavaScript y React para el frontend, junto con gestores de bases de datos como MySQL. Además, manejo de Spring Boot y Spring Security en Java para la implementación de sistemas seguros y eficientes.', enlace:'http://www.direccion.com'}
]);
</script>

<template>
    <ul>
        <li v-for="(item, index) in educacion" :key="index" :style="{ '--fecha-color': fechaColor[index].color}">
            <div class="fecha">{{ item.fecha }}</div>
            <h3 class="title">{{ item.title }}</h3>
            <div class="descripcion">{{ item.descripcion }}</div>
            <a class="enlace" :href="item.enlace" target="_blank">Saber más</a>
        </li>
    </ul>
</template>

<style scoped>
/* Estilos generales */
@import url("https://fonts.googleapis.com/css2?family=Poppins:wght@300;500;700&display=swap");
*,
*::before,
*::after {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

body {
  --color: #4B0F20; /* Color de texto principal en un tono rosado oscuro */
  --bgColor: #FEE9E5; /* Fondo claro en tono rosado suave */
  min-height: 100vh;
  display: grid;
  align-content: center;
  gap: 2rem;
  padding: 2rem;
  font-family: "Poppins", sans-serif;
  color: var(--color);
  background: var(--bgColor);
}

/* Estilos para la lista */
ul {
  margin-top: 2rem;
  --col-gap: 2rem;
  --row-gap: 2rem;
  --line-w: 0.25rem;
  display: grid;
  grid-template-columns: var(--line-w) 1fr;
  grid-auto-columns: max-content;
  column-gap: var(--col-gap);
  list-style: none;
  width: min(60rem, 90%);
  margin-inline: auto;
}

/* Estilo para la línea vertical que conecta los elementos de la lista */
ul::before {
  content: "";
  grid-column: 1;
  grid-row: 1 / span 20;
  background: rgb(225, 225, 225);
  border-radius: calc(var(--line-w) / 2);
}

/* Estilo para cada ítem de la lista */
ul li {
  grid-column: 2;
  --inlineP: 1.5rem;
  margin-inline: var(--inlineP);
  grid-row: span 2;
  display: grid;
  grid-template-rows: min-content min-content min-content;
  background: #FFF5F7; /* Fondo muy suave para contraste */
  border-radius: 8px; /* Bordes redondeados */
  padding: 1rem; /* Espaciado interno */
  box-shadow: 0 2px 8px rgba(0, 0, 0, 0.2); /* Sombra más marcada */
}

/* Estilo para la fecha dentro de cada ítem */
ul li .fecha {
  --dateH: 3rem;
  height: var(--dateH);
  margin-inline: calc(var(--inlineP) * -1);
  text-align: center;
  background-color: var(--fecha-color); /* Colores personalizados de la fecha */
  color: #FFFFFF; /* Texto blanco */
  font-size: 1.25rem;
  font-weight: 700;
  display: grid;
  place-content: center;
  position: relative;
  border-radius: calc(var(--dateH) / 2) 0 0 calc(var(--dateH) / 2);
}

/* Estilos para el título y descripción */
.title {
  color: #4B0F20; /* Color del título en tono rosado oscuro */
  font-weight: 500;
  padding-inline: 1.5rem;
  background: #FFF5F7; /* Fondo suave */
}

.descripcion {
  color: #B76E8E; /* Color rosado claro para contraste */
  font-weight: 300;
  padding-inline: 1.5rem;
  background: #FFF5F7; /* Fondo suave */
}

/* Estilos para el enlace */
.enlace {
  color: #FF6F91; /* Color rosado brillante para el enlace */
  text-decoration: none; /* Sin subrayado */
}

.enlace:hover {
  text-decoration: underline; /* Subrayado al pasar el mouse */
}

/* Media query para pantallas anchas (40rem o más) */
@media (min-width: 40rem) {
  ul {
    grid-template-columns: 1fr var(--line-w) 1fr;
  }
  ul::before {
    grid-column: 2;
  }
  ul li:nth-child(odd) {
    grid-column: 1;
  }
  ul li:nth-child(even) {
    grid-column: 3;
  }
  ul li:nth-child(2) {
    grid-row: 2/4;
  }
  /* Ajustes para los ítems impares */
  ul li:nth-child(odd) .fecha::before {
    clip-path: polygon(0 0, 100% 0, 100% 100%);
    left: 0;
  }
  ul li:nth-child(odd) .fecha::after {
    left: calc(100% + var(--col-gap) + var(--line-w) / 2);
  }
  ul li:nth-child(odd) .fecha {
    border-radius: 0 calc(var(--dateH) / 2) calc(var(--dateH) / 2) 0;
  }
}


</style>
