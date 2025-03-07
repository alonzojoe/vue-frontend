<template>
    <input :type="type"
        class="w-full px-2 py-1 text-md bg-white border outline-none focus:ring-0 border-gray-300 rounded-md placeholder-gray-400 focus:ring-indigo-500" />
</template>

<script setup>
const props = defineProps({
    type: String
})
</script>

<style scoped></style>