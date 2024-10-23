<script setup>
import { ref } from 'vue';

var habilidades = ref([]);
habilidades.value = ([

]);
</script>

<template>
    <div class="skills-contenedor">
        <div class="skills-categoria">
            <h3>Lenguaje de Programación</h3>
            <ul class="skills">
                <li class="skill">
                    <img src="/src/components/icons/javascript-svgrepo-com.svg" alt="JavaScript">
                    <span>JavaScript: Avanzado</span>
                </li>
                <li class="skill">
                    <img src="/src/components/icons/python-svgrepo-com.svg" alt="Python">
                    <span>Python: Intermedio</span>
                </li>
                <li class="skill">
                    <img src="/src/components/icons/html-5-svgrepo-com.svg" alt="Html">
                    <span>HTML: Avanzado</span>
                </li>
                <li class="skill">
                    <img src="/src/components/icons/css-3-svgrepo-com.svg" alt="Css">
                    <span>CSS: Avanzado</span>
                </li>
                <li class="skill">
                    <img src="/src/components/icons/sql.svg" alt="Sql">
                    <span>SQL: Intermedio</span>
                </li>
                <li class="skill">
                    <img src="/src/components/icons/java.svg" alt="Java">
                    <span>Java: Intermedio</span>
                </li>
            </ul>
        </div>
        <div class="skills-categoria">
            <h3>Frameworks y Librerias</h3>
            <ul class="skills">
                <li class="skill">
                    <img src="/src/components/icons/react.svg" alt="React">
                    <span>React: Intermedio</span>
                </li>
                <li class="skill">
                    <img src="/src/components/icons/vue.svg" alt="Vue">
                    <span>Vue: Intermedio</span>
                </li>
                <li class="skill">
                    <img src="/src/components/icons/bootstrap.svg" alt="BootStrap">
                    <span>Bootstrap: Intermedio</span>
                </li>
                <li class="skill">
                    <img src="/src/components/icons/spring.svg" alt="SpringBoot">
                    <span>Spring Boot: Intermedio</span>
                </li>
            </ul>
        </div>
        <div class="skills-categoria">
            <h3>Herramientas y Software</h3>
            <ul class="skills">
                <li class="skill">
                    <img src="/src/components/icons/git.svg" alt="Git">
                    <span>Git: Avanzado</span>
                </li>
                <li class="skill">
                    <img src="/src/components/icons/vsc.svg" alt="Visual Studio Code">
                    <span>Visual Studio Code: Avanzado</span>
                </li>
            </ul>
        </div>
        <div class="skills-categoria">
            <h3>Idiomas</h3>
            <ul class="skills">
                <li class="skill">
                    <img src="/src/components/icons/argentina.svg" alt="Git">
                    <span>Español: Nativo</span>
                </li>
                <li class="skill">
                    <img src="/src/components/icons/eeuu.png" alt="Visual Studio Code">
                    <span>Ingles: Intermedio</span>
                </li>
            </ul>
        </div>
    </div>
</template>

<style scoped>
.skills-contenedor{
    padding: 2rem;
}

.skills-categoria{
    margin-bottom: 20px;
}

.skills-categoria h3 {
    display: flex;
    justify-content: left;
    margin-bottom: 10px;
    font-size: 1.5em;
    color: #d1235c;
    font-size: 1.5em;
    font-weight: bold;
}

.skills{
    display: flex;
    justify-content: space-evenly;
    flex-wrap: wrap;
    gap: 20px;
}

.skill{
    display: flex;
    justify-content: center;
    align-content: center;
    gap: 10px;
    padding: 0.3em;
    border-radius: 8px;
    box-shadow: 0px 4px 12px #f8c2c1;
    flex: 1 1 200px;
    max-width: 250px;
}

.skill:hover {
    background-color: #f8c2c1;
    font-size: 1.3em;
    transition: 2s ease;
}

.skill img {
    width: 35px;
    height: 35px;
}

.skill span{
    font-size: 1em;
    color: #333;
}

@media (max-width: 768px) {
    .skills-categoria h3 {
        justify-content: center;
    }

    .skill {
        justify-content: center;
    }
}

</style>