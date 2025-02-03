<template>
  <div class="flex flex-col items-center justify-center h-screen flex-1 bg-gray-600 p-4">
    <form @submit.prevent="">
      <input
        class="bg-white border border-gray-300 rounded-lg p-1"
        type="password"
        v-model="test.sigma"
      />
      <button
        class="bg-blue-500 border border-blue-500 hover:border-blue-600 hover:bg-blue-600 hover:cursor-pointer rounded-lg p-1 m-1"
        type="submit"
      >
        Submit
      </button>
    </form>
    <div class="text-white" v-if="!/[A-Z]/.test(test.sigma)">No skibidi capital</div>
    <div class="text-white" v-if="!/\d/.test(test.sigma)">No skibidi numbah</div>
    <div class="text-white" v-if="test.sigma.length < 9">Not more than skibidi eight</div>
  </div>
</template>

<script setup>
import { reactive } from 'vue'

const test = reactive({ sigma: '' })
</script>
