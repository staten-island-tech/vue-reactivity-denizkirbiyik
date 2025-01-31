<template>
  <div class="flex items-center justify-center h-screen flex-1 bg-gray-600 p-4">
    <form @submit.prevent="">
      <input++
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
    <h1>{{ test }}</h1>
  </div>
</template>

<script setup>
import { reactive } from 'vue'

const test = reactive({ sigma: '' })
</script>
