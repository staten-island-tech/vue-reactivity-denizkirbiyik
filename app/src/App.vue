<template>
  <div class="flex h-screen">
    <MainContainer />

    <SideBar />
  </div>
</template>

<script>
import MainContainer from '@/components/MainContainer.vue'
import SideBar from '@/components/SideBar.vue'

export default {
  components: {
    MainContainer,
    SideBar,
  },
}
</script>
