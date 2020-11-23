<template>
  <div>
    <Sidebar />
    <div class="transparent"></div>

    <Nuxt />
  </div>
</template>
<script>
import Sidebar from '@/components/Sidebar'
export default {
  components: {
    Sidebar,
  },
  data() {
    return {
      isMobile: '',
    }
  },
  mounted() {
    this.isMobile = screen.width > 760 ? false : true
  },
}
</script>
<style lang="scss">
.transparent {
  background: transparent;
  height: 59.6px;
}
.transparent-side {
  background: transparent;
  width: 260px;
  height: 100%;
  position: absolute;
  left: 0;
  top: 0;
}
</style>
