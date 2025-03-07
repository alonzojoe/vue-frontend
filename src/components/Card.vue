<template>
    <div class="card bg-white rounded-md p-20">
        <slot></slot>
    </div>
</template>

<script setup>

</script>

<style scoped>
.card {
    height: fit-content;
    width: 60vw;
    box-shadow: 0px 0px 0px 8px rgba(255, 255, 255, 0.3);
}

@media screen and (max-width: 768px) {
    .card {
        width: 80vw;
    }
}

@media screen and (max-width: 450px) {
    .card {
        width: 90vw;
    }
}
</style>