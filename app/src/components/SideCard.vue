<template>
  <div class="w-[90%] h-[200px] rounded-lg bg-gray-600 text-white p-5">
    <input
      value="skibidi"
      tabindex="-1"
      class="!outline-none caret-transparent cursor-default"
      v-bind:type="b ? 'password' : 'text'"
      readonly="readonly"
    />
    <button
      @click="b = !b"
      class="bg-blue-500 border border-blue-500 hover:border-blue-600 hover:bg-blue-600 hover:cursor-pointer rounded-lg p-1 m-1"
    >
      skib
    </button>
  </div>
</template>

<script>
import { ref } from 'vue'

const b = ref(true)
/*
export default {
  data() {
    return {
      b: true,
    }
  },
}
*/
</script>
