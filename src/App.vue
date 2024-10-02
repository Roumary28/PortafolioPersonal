<script setup>
import NavBar from './components/NavBar.vue';
import DatosPersonales from './components/DatosPersonales.vue';
import EducacionComponent from './components/EducacionComponent.vue';
import ExperienciaComponent from './components/ExperienciaComponent.vue';
</script>

<template>
  <header>
    <!-- Barra de navegacion-->
    <NavBar/>
    <!-- Datos Personales -->
     <DatosPersonales/>
  </header>
  <main>
    <section id="educacion">
      <h2>Educacion - Cursos</h2>
      <EducacionComponent/>
    </section>
    <section id="experiencia">
      <h2>Experiencia</h2>
      <ExperienciaComponent/>
    </section>
    <section id="proyectos">
      <h2>Proyectos</h2>
    </section>
    <section id="habilidades">
      <h2>Habilidades</h2>
    </section>
    <section id="intereses">
      <h2>Intereses</h2>
    </section>
  </main>
</template>

<style scoped>
section h2 {
    font-size: 2.5rem; /* Tamaño destacado */
    color:#b23a48; /* Rosado más oscuro */
    font-weight: bold;
    text-align: center;
    margin-bottom: 1rem;
    padding-bottom: 0.5rem;
    position: relative;
    text-shadow: 1px 1px 3px rgba(140, 74, 88, 0.5); /* Sombra suave para profundidad */
}

/* Línea decorativa debajo del h2 */
section h2::after {
    content: "";
    display: block;
    width: 50px;
    height: 4px;
    background-color: #4b0f20; /* Rosado mucho más oscuro para contraste */
    margin: 0.5rem auto 0;
    border-radius: 2px; /* Bordes redondeados */
}

section h2:hover {
    color: #a65366; /* Un tono de rosado oscuro ligeramente más suave en hover */
    text-shadow: 2px 2px 5px rgba(140, 74, 88, 0.7); /* Más sombra en hover */
}


</style>
