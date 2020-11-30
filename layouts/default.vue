<template>
  <div>
    <Sidebar />
    <div class="transparent"></div>
    <!-- <div class="transparent-side"></div> -->
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
  height: 88.4px;
}
.transparent-side {
  background: #fff;

  height: 200vh;
  // position: absolute;
  // left: 0;
  // top: 0;
}
</style>
