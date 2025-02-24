<template>
  <div class="flex flex-col items-center justify-center h-screen flex-1 bg-gray-600 p-4">
    <form @submit.prevent="addPass">
      <input
        class="bg-white border border-gray-300 rounded-lg p-1"
        type="password"
        v-model="cur.sigma"
      />
      <button
        class="bg-blue-500 border border-blue-500 hover:border-blue-600 hover:bg-blue-600 hover:cursor-pointer rounded-lg p-1 m-1"
        type="submit"
      >
        Submit
      </button>
    </form>
    <div class="text-white" v-if="!/[A-Z]/.test(cur.sigma)">No capital</div>
    <div class="text-white" v-if="!/\d/.test(cur.sigma)">No number</div>
    <div class="text-white" v-if="cur.sigma.length < 9">Not more than eight</div>
  </div>
</template>

<script setup>
import { reactive } from 'vue'
import { passes } from '@/components/Passes.vue'

const cur = reactive({ sigma: '' })

const addPass = () => {
  if (/[A-Z]/.test(cur.sigma) && /\d/.test(cur.sigma) && cur.sigma.length > 8) {
    passes.push(cur.sigma)
    cur.sigma = ''
  }
}
</script>
