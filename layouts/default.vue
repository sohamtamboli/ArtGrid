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
html {
  font-family: 'Gill Sans', 'Gill Sans MT', Calibri, 'Trebuchet MS', sans-serif;
  box-sizing: border-box;
  background: #212121;
  color: #fff;
}

*,
*::before,
*::after {
  box-sizing: border-box;
  margin: 0;
}
</style>
