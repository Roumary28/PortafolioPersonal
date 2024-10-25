<script setup>
import { ref } from 'vue';

var intereses = ref([
    {id:1, interes:'🎸 Guitarra:', descripcion: 'Estoy en un emocionante viaje musical, aprendiendo acordes, deslumbrantes canciones y melodías que tocan el corazón.'},
    {id:2, interes:'🛼 Patinaje Inline:', descripcion: ' Me encanta deslizarme con libertad por parques y ciudades, disfrutando del viento en el rostro mientras exploro skateparks.'},
    {id:3, interes:'👨‍👧 Momentos en familia:', descripcion: 'Valoro profundamente cada instante compartido con mi familia, dedicando tiempo especial a mi hija, creando recuerdos inolvidables.'}
]);

</script>

<template>
    <div class="intereses-contenedor">
        <ul class="contenedor-lista" >
            <li class="item" v-for="inte in intereses" :key="inte.id" > <!-- el vfor esta en el li para que un elemento se vea abajo del otro-->
                 <span class="negrita">{{ inte.interes }}</span> {{ inte.descripcion }}
            </li>
        </ul>
    </div>
</template>


<style scoped>
.negrita {
    font-weight: bold; /* Asegura que el texto esté en negrita */
}

.intereses-contenedor {
    display: flex;
    justify-content: center;
    align-items: center;
    margin: 0 auto;
    max-width: 85%;
    padding: 2rem;
    background-color: #f8c2c1; /* Fondo rosa pastel */
    border-radius: 10px; /* Bordes redondeados */
    box-shadow: 0 4px 15px rgba(0, 0, 0, 0.1); /* Sombra más suave */
}

.contenedor-lista {
    list-style-type: none;
    padding: 0;
    margin: 0;
    color: #b85f6d; /* Color de texto principal, un tono más suave */
    font-size: 1.4rem;
    text-shadow: 1px 1px 3px rgba(0, 0, 0, 0.3); /* Sombra de texto más suave */
}

.item {
    margin-bottom: 1rem;
    transition: transform 0.3s, color 0.3s, background-color 0.3s; /* Transición suave */
    padding: 0.5rem; /* Espaciado interno */
    border-radius: 5px; /* Bordes redondeados */
}

.item:hover {
    transform: translateY(-3px); /* Levanta el elemento al pasar el mouse */
    color: #ff6f8a; /* Color de texto al hacer hover, un tono más intenso */
    background-color: rgba(255, 121, 198, 0.2); /* Fondo suave al hacer hover */
}
</style>

