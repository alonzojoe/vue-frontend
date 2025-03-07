<script setup>
import { computed } from 'vue';
import Captcha from './components/Captcha.vue';
import Card from "./components/Card.vue"
import backgroundImg from "./assets/blue-bg.avif"
import vipTutorsLogo from "./assets/viptutors.png"


const background = computed(() => ({
  background: `url(${backgroundImg})`,
  backgroundSize: `cover`,
  backgroundPosition: `center`,
  backgroundRepeat: `no-repeat`
}))

</script>

<template>
  <div class="min-h-[100dvh] flex items-center justify-center" :style="background">
    <Card>
      <div class="flex gap-6 flex-nowrap">
        <div class="flex-grow">
          <img :src="vipTutorsLogo" class="h-auto w-[15rem]" />
        </div>
        <div class="flex-grow">
          <h2 class="text-left text-2xl font-bolder mb-10">Sign in to your account</h2>
          <div class="mb-3">
            <label class="font-medium block mb-1">Username / Email Address / Mobile</label>
            <input type="text"
              class="w-full px-2 py-1 text-md bg-white border outline-none focus:ring-0 border-gray-300 rounded-md placeholder-gray-400 focus:ring-indigo-500" />
          </div>
          <div class="mb-3">
            <label class="font-medium block mb-1">Password</label>
            <input type="password"
              class="w-full px-2 py-1 text-md bg-white border outline-none focus:ring-0 border-gray-300 rounded-md placeholder-gray-400 focus:ring-indigo-500" />
          </div>
          <div class="mb-3">
            <p class="text-sm">Forgot your password? <a href="#" class="text-orange-400 font-bold">Reset Password</a>
            </p>
          </div>
          <div class="mb-3">
            <Captcha />
          </div>
          <div class="mb-3">
            <label class="font-medium block mb-1">Enter the characters you see above</label>
            <input type="text"
              class="w-full px-2 py-1 text-md bg-white border outline-none focus:ring-0 border-gray-300 rounded-md placeholder-gray-400 focus:ring-indigo-500" />
          </div>
          <div class="my-8">
            <button
              class="bg-blue-800 px-3 py-2 w-full rounded-3xl text-white hover:bg-blue-900 cursor-pointer">Login</button>
          </div>
          <div class="mb-3">
            <p class="text-sm">Don't have and account? <a href="#" class="text-orange-400 font-bold">Create an
                account</a>
            </p>
          </div>
        </div>
      </div>
    </Card>
  </div>

</template>

<style scoped></style>
