<template>
  <div>
    <Sidebar />
    <Nuxt />
  </div>
</template>
<script>
import Sidebar from '@/components/Sidebar'

export default {
  components: {
    Sidebar,
  },
}
</script>
<style>
* {
  box-sizing: border-box;
  background: #212121;
  color: #fff;
}
</style>
