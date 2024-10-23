<script setup>
import { ref } from 'vue';

var proyectos = ref([]);

proyectos.value = ([
    {nombre: 'Ecommerce', descripcion: 'Tienda de ropa online', link:'https://www.tienda.com', git:'https://github.com/Roumary28/tienda-app', imagen: '/src/assets/tienda.png'}, 
    {nombre: 'Pagina Inmobiliaria' , descripcion: 'Página Web de inmobiliaria', link:'https://www.inmobiliaria.com', git:'https://github.com/Roumary28/appInmobiliaria', imagen: '/src/assets/inmobiliaria.png'}
]);
</script>

<template>
    <div class="galeria">
        <div class="proyecto" v-for="(proyecto, index) in proyectos" :key="index">
            <img class="imagen-proyecto" :src="proyecto.imagen" :alt="`Imagen del proyecto ${proyecto.nombre}`">
            <div class="proyecto-info">
                <h3>{{ proyecto.nombre }}</h3>
                <p>{{ proyecto.descripcion }}</p>
                <div class="proyecto-links">
                    <a :href="proyecto.link" class="btn-ver-mas" target="_blank" rel="noopener noreferrer">Ver proyecto</a>
                    <a :href="proyecto.git" class="github-link" target="_blank" rel="noopener noreferrer">Ver Código en GitHub</a>
                </div>
            </div>
        </div>
    </div>
</template>


<style scoped>
.galeria {
    display: flex;
    flex-wrap: wrap;
    gap: 20px;
    justify-content: center;
    background-image: url('/src/assets/fondoproyectos.jpg');
    width: 100%;
    height: 100vh;
    background-size: cover;
    background-position: center;
    background-repeat: no-repeat;
}

.imagen-proyecto {
    width: 100%; /* Asegura que la imagen ocupe el ancho completo del contenedor */
    height: 200px; /* Define un alto fijo para las imágenes */
    object-fit: cover; /* Recorta la imagen para que llene el área sin distorsión */
}


.proyecto {
    display: flex;
    flex-direction: column;
    border: 2px solid #f2b6b6;
    border-radius: 8px;
    overflow: hidden;
    background-color: rgba(255, 228, 230, 0.8);
    max-width: 300px; /* Define el ancho máximo */
    width: 100%; /* Ocupa el 100% del ancho disponible dentro del contenedor */
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
    transition: transform 0.3s ease;
}


.proyecto:hover {
    transform: translateY(-5px); /* Efecto elevación */
}

.proyecto img {
    width: 100%;
    height: auto;
    display: block;
}

.proyecto-info {
    padding: 15px;
    text-align: center;
}

.proyecto-info h3 {
    margin: 10px 0;
    font-size: 1.3em;
    color: #b23a48; /* Rosa intenso */
}

.proyecto-info p {
    margin: 10px 0;
    font-size: 1em;
    color: #d17575; /* Rosa suave */
}

.proyecto-links {
    display: flex;
    flex-direction: column;
    gap: 10px;
    margin-top: 10px;
}

.proyecto-links .btn-ver-mas {
    background-color: #b23a48; /* Rosa intenso */
    color: #fff;
    padding: 10px 15px;
    border-radius: 5px;
    text-decoration: none;
    transition: background-color 0.3s;
}

.proyecto-links .btn-ver-mas:hover {
    background-color: #922838; /* Rosa más oscuro */
}

.proyecto-links .github-link {
    color: #922838; /* Rosa más oscuro */
    text-decoration: none;
    font-size: 0.9em;
}

.proyecto-links .github-link:hover {
    text-decoration: underline;
}

</style>