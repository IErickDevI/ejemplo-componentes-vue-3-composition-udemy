<script setup>

defineProps(['inicio', 'fin', 'maxLength'])

/* defineProps({
    nextPaginate: Function,
    prevPaginate: Function
}) */

const emit = defineEmits(['next', 'prev'])

</script>

<template>

    <div class="btn-group" role="group" aria-label="Basic example">
        <!--  <button type="button" class="btn btn-outline-primary" @click="prevPaginate">Previous</button>
        <button type="button" class="btn btn-outline-primary" @click="nextPaginate">Next</button> -->
        <button type="button" class="btn btn-outline-primary" :disabled="inicio === 0" @click="emit('prev')">Previous {{ inicio }}</button>
        <button type="button" class="btn btn-outline-primary" :disabled="fin === maxLength " @click="emit('next')">Next {{ fin }}</button>
    </div>

</template>