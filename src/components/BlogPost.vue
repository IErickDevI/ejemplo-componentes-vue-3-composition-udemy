<script setup>

/* defineProps(['title', 'id', 'body', 'colorText'])*/

defineProps({
    title: String,
    id: Number,
    body: {
        type:String,
        default: "Sin Descripcion",
    },
    cambiarFavorito: Function
});

const emit = defineEmits(['cambiarFavoritoNombre'])
</script>

<template>
    <div class="card">
        <div class="card-body">
            <!-- funciona con cualquiera de las dos, son dos opciones correctas  -->
            <!-- <h5 class="card-title" :class="colorText">{{ id }} - {{ title }}</h5> -->
            <!-- <h5 class="card-title" :class="`text-${colorText}`">{{ id }} - {{ title }}</h5> -->
            <h5 class="card-title">{{ id }} - {{ title }}</h5>
            <p>{{ body }}</p>
            <button @click="cambiarFavorito(title)" class="btn btn-outline-primary">Favorito</button>
        </div>
    </div>
</template>