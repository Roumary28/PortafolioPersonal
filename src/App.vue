<script setup>
import NavBar from './components/NavBar.vue';
import DatosPersonales from './components/DatosPersonales.vue';
import EducacionComponent from './components/EducacionComponent.vue';
import ExperienciaComponent from './components/ExperienciaComponent.vue';
import ProyectosComponent from './components/ProyectosComponent.vue';
import HabilidadesComponent from './components/HabilidadesComponent.vue'; 
import InteresesComponent from './components/InteresesComponent.vue';
</script>

<template>
  <header id="top">
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
      <ProyectosComponent/>
    </section>
    <section id="habilidades">
      <h2>Habilidades</h2>
      <HabilidadesComponent/>
    </section>
    <section id="intereses">
      <h2>Intereses</h2>
      <InteresesComponent/>
    </section>
  </main>
  <footer>
    <a href="#top"> Inicio </a>
    <p>© 2024 Danna Martinez - Portafolio Web </p>
  </footer>
</template>

<style scoped>
section h2 {
    font-size: 2.5rem; /* Tamaño destacado */
    color: #b23a48; /* Rosado más oscuro */
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

/* Espaciado entre la última sección y el footer */
section {
    margin-bottom: 4rem; /* Añade espacio inferior a la sección */
}

/* Estilos para el footer */
footer {
    display: flex;
    flex-direction: column;
    align-items: center;
    padding: 2rem;
    font-size: 1.3rem;
    background-color: #f8c2c1; /* Fondo en rosa pastel para combinar con el estilo general */
    color: #4b0f20; /* Color de texto más oscuro para contraste */
    box-shadow: 0 4px 15px rgba(0, 0, 0, 0.1); /* Sombra suave para dar profundidad */
    border-top: 4px solid #b23a48; /* Borde superior en rosa oscuro para separar visualmente */
    text-shadow: 1px 1px 2px rgba(0, 0, 0, 0.3); /* Sombra ligera en el texto */
    margin-top: 4rem; /* Espacio adicional entre el footer y la sección anterior */
}

footer a {
    color: #b85f6d; /* Color del enlace que armoniza con el esquema */
    text-decoration: none;
    transition: color 0.3s;
}

footer a:hover {
    color: #ff79c6; /* Color más vibrante al hacer hover */
}
</style>
