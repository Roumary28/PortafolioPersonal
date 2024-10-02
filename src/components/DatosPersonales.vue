<script setup>
const title = 'Rosario Danna Martinez Baez';
const descripcion = 'Técnica Universitaria en Programación - UTN FRSR';
const residencia = 'Ciudad de Mendoza, Mendoza, Argentina';
const presentacion = '¡Hola! Bienvenido a mi portafolio de proyectos. Soy una desarrolladora web con experiencia en el desarrollo de aplicaciones web y móviles.';
const redesSociales = [
    { id: 1, name: 'linkedin', src: '/src/assets/linkedin_icon.svg', url: 'https://www.linkedin.com/in/rosariodannamartinez/' },
    { id: 2, name: 'Instagram', src: '/src/assets/instagram_icon.svg', url: 'https://www.instagram.com/dannamartinezbaez/' },
    { id: 3, name: 'github', src: '/src/assets/github_icon.svg', url: 'https://github.com/Roumary28' },
    { id: 4, name: 'curriculum', src: '/src/assets/cv_resume_icon.svg', url: 'https://drive.google.com/file/d/1YqIJfujoJUCaJOq8asoWjFC0_2eZvJUS/view?usp=sharing' },
];
const telefono = '+54 9 2615522560';
</script>

<template>
    <section class="datos-personales">
        <div class="card">
            <h1>{{ title }}</h1>
            <h2>{{ descripcion }}</h2>
            <p>{{ presentacion }}</p>
            <ul class="container-lista">
                <li v-for="red in redesSociales" :key="red.id">
                    <a :href="red.url" target="_blank">
                        <img class="icon-redsocial" :src="red.src" width="35rem" :alt="red.name">
                    </a>
                </li>
            </ul>
            <h3>☎ Mi Teléfono personal: {{ telefono }}</h3>
            <h4>{{ residencia }}</h4>
        </div>
    </section>
</template>

<style scoped>
h1 {
    font-size: 3.5rem; /* Tamaño aumentado para mayor impacto */
    color: #b23a48; /* Rosa oscuro intenso */
    font-weight: bold;
    margin-bottom: 0.5rem;
    text-shadow: 2px 2px 5px rgba(178, 58, 72, 0.4); /* Sombra para destacar */
}

h2 {
    font-size: 2.2rem; 
    color: #a65353; /* Rosa oscuro suave */
    margin-bottom: 1rem;
}

p {
    font-size: 1.3rem;
    font-weight: 500;
    color: #b5838d; /* Rosa oscuro suave */
    margin-bottom: 2rem;
}

.card {
    background-color: #f0dbd7; /* Rosa claro */
    border-radius: 15px;
    padding: 20px;
    margin: 10px;
    text-align: center;
    box-shadow: 0 10px 20px rgba(209, 167, 160, 0.5); /* Sombra */
    transition: transform 0.3s ease; /* Efecto hover */
}

.card:hover {
    transform: translateY(-10px); /* Efecto de elevación */
}

.container-lista {
    display: flex;
    justify-content: center;
    list-style: none;
    padding: 0;
    margin: 0 0 2rem 0;
}

.icon-redsocial {
    align-items: center;
    background-color: #f8c2c1; /* Rosa pastel */
    border-radius: 50%;
    padding: 8px;
    margin: 5px;
    box-shadow: 0 5px 10px rgba(251, 203, 203, 0.5); /* Sombra suave */
    transition: background-color 0.3s ease, transform 0.3s ease; /* Animación suave */
}

.icon-redsocial:hover {
    background-color: #d1a7a0; /* Fondo rosa viejo */
    transform: scale(1.1); /* Agrandamiento al hacer hover */
}

h3 {
    font-size: 1.4rem;
    color: #d1a7a0; /* Rosa viejo */
    margin-bottom: 0.5rem;
}

h4 {
    font-size: 1.1rem;
    color: #b5838d; /* Rosa oscuro suave */
}
</style>
