<template>
    <div class="flex items-center gap-5">
        <p class="bg-green-700 opacity-90 text-2xl tracking-[0.6rem] text-white px-5 py-2">{{ captcha }}</p><span
            class="cursor-pointer text-3xl text-dark" @click="generateCaptcha">
            ⟳
        </span>
    </div>
</template>

<script setup>
import { ref, onMounted } from 'vue';

const captcha = ref("")

const generateCaptcha = () => {
    const characters = 'ABCDEFGHIJKLMNOPQRSTUVWXYZ0123456789';
    let randomString = '';
    for (let i = 0; i < 6; i++) {
        const randomIndex = Math.floor(Math.random() * characters.length);
        randomString += characters[randomIndex];
    }
    captcha.value = randomString;
}

onMounted(() => {
    generateCaptcha()
})

</script>

<style lang="scss" scoped></style>