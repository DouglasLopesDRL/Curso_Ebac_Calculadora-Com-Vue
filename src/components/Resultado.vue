<script setup>
    const props = defineProps(['resultado']);
</script>

<template>
    <div class="text-center p-5 mb-4 mt-4 bg-light rounded-3">
        <p class="fs-2">Resultado: </p>
        <p class="fs-4">{{ props.resultado }}</p>
    </div>
</template>