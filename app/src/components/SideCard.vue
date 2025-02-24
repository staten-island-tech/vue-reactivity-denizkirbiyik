<template>
  <div
    class="w-[90%] h-[200px] rounded-lg bg-gray-600 text-white p-5 m-2 flex flex-col justify-between"
  >
    <div class="flex items-center">
      <input
        :value="pass"
        tabindex="-1"
        class="!outline-none caret-transparent cursor-default bg-transparent flex-grow"
        :type="b ? 'password' : 'text'"
        readonly="readonly"
      />
      <button
        @click="b = !b"
        class="bg-blue-500 border border-blue-500 hover:border-blue-600 hover:cursor-pointer rounded-lg p-1 m-1"
      >
        view
      </button>
    </div>
    <div class="flex justify-end">
      <button
        @click="$emit('remove', pass)"
        class="bg-red-500 border border-red-500 hover:border-red-600 hover:cursor-pointer rounded-lg p-1 m-1"
      >
        delete
      </button>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    pass: {
      type: String,
      required: true,
    },
  },
  data() {
    return {
      b: true,
    }
  },
}
</script>
