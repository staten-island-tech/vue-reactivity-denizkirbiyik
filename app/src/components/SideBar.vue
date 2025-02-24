<template>
  <div class="w-100 bg-gray-800 shadow-lg border-l p-5 flex items-center flex-col">
    <h1 class="text-white text-2xl font-semibold text-center">History</h1>
    <hr class="my-4 border-gray-600 w-full" />
    <SideCard v-for="p in passes" :key="p.id" :pass="p" @remove="removePass" />
  </div>
</template>

<script>
import SideCard from '@/components/SideCard.vue'
import { passes } from '@/components/Passes.vue'

export default {
  components: {
    SideCard,
  },
  data() {
    return {
      passes,
    }
  },
  methods: {
    removePass(pass) {
      const index = this.passes.indexOf(pass)
      if (index > -1) {
        this.passes.splice(index, 1)
      }
    },
  },
}
</script>
