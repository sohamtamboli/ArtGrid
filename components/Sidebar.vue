<template>
  <div class="hidden">
    <vs-navbar
      shadow
      color="#212121"
      text-white
      center-collapsed
      v-model="active"
    >
      <template #left>
        <vs-button v-show="isMobile" @click="openMenu" flat dark>
          <div class="menu">
            <i class="icon">
              <svg
                xmlns="http://www.w3.org/2000/svg"
                viewBox="0 0 20 20"
                fill="currentColor"
              >
                <path
                  fill-rule="evenodd"
                  d="M3 5a1 1 0 011-1h12a1 1 0 110 2H4a1 1 0 01-1-1zM3 10a1 1 0 011-1h6a1 1 0 110 2H4a1 1 0 01-1-1zM3 15a1 1 0 011-1h12a1 1 0 110 2H4a1 1 0 01-1-1z"
                  clip-rule="evenodd"
                /></svg
            ></i>
          </div>
        </vs-button>
      </template>
      <template #right>
        <vs-button flat circle color="#ff6600" size="large">Login</vs-button>
      </template>
    </vs-navbar>
    <vs-sidebar
      absolute
      v-model="active"
      :open="openSidebar"
      background="#212121"
      textWhite
    >
      <vs-button v-show="isMobile" @click="closeMenu" flat dark>
        <div class="menu">
          <i class="icon">
            <svg
              xmlns="http://www.w3.org/2000/svg"
              viewBox="0 0 20 20"
              fill="currentColor"
            >
              <path
                fill-rule="evenodd"
                d="M4.293 4.293a1 1 0 011.414 0L10 8.586l4.293-4.293a1 1 0 111.414 1.414L11.414 10l4.293 4.293a1 1 0 01-1.414 1.414L10 11.414l-4.293 4.293a1 1 0 01-1.414-1.414L8.586 10 4.293 5.707a1 1 0 010-1.414z"
                clip-rule="evenodd"
              /></svg
          ></i>
        </div>
      </vs-button>
      <template #logo>
        <!-- ...img logo -->
      </template>

      <vs-sidebar-item id="home"
        ><nuxt-link to="/" class="list-item">
          <i class="icon">
            <svg
              xmlns="http://www.w3.org/2000/svg"
              viewBox="0 0 20 20"
              fill="currentColor"
              class="icon"
            >
              <path
                d="M10.707 2.293a1 1 0 00-1.414 0l-7 7a1 1 0 001.414 1.414L4 10.414V17a1 1 0 001 1h2a1 1 0 001-1v-2a1 1 0 011-1h2a1 1 0 011 1v2a1 1 0 001 1h2a1 1 0 001-1v-6.586l.293.293a1 1 0 001.414-1.414l-7-7z"
              /></svg
          ></i>
          <h3>Home</h3>
        </nuxt-link>
      </vs-sidebar-item>

      <vs-sidebar-item id="Profile">
        <nuxt-link to="/" class="list-item">
          <i class="icon">
            <svg
              xmlns="http://www.w3.org/2000/svg"
              viewBox="0 0 20 20"
              fill="currentColor"
            >
              <path
                fill-rule="evenodd"
                d="M10 9a3 3 0 100-6 3 3 0 000 6zm-7 9a7 7 0 1114 0H3z"
                clip-rule="evenodd"
              /></svg
          ></i>
          <h3>Profle</h3>
        </nuxt-link>
      </vs-sidebar-item>
      <vs-sidebar-item id="About">
        <nuxt-link to="/" class="list-item">
          <i class="icon">
            <svg
              xmlns="http://www.w3.org/2000/svg"
              viewBox="0 0 20 20"
              fill="currentColor"
            >
              <path
                fill-rule="evenodd"
                d="M6.267 3.455a3.066 3.066 0 001.745-.723 3.066 3.066 0 013.976 0 3.066 3.066 0 001.745.723 3.066 3.066 0 012.812 2.812c.051.643.304 1.254.723 1.745a3.066 3.066 0 010 3.976 3.066 3.066 0 00-.723 1.745 3.066 3.066 0 01-2.812 2.812 3.066 3.066 0 00-1.745.723 3.066 3.066 0 01-3.976 0 3.066 3.066 0 00-1.745-.723 3.066 3.066 0 01-2.812-2.812 3.066 3.066 0 00-.723-1.745 3.066 3.066 0 010-3.976 3.066 3.066 0 00.723-1.745 3.066 3.066 0 012.812-2.812zm7.44 5.252a1 1 0 00-1.414-1.414L9 10.586 7.707 9.293a1 1 0 00-1.414 1.414l2 2a1 1 0 001.414 0l4-4z"
                clip-rule="evenodd"
              /></svg
          ></i>
          <h3>About the Creator</h3>
        </nuxt-link>
      </vs-sidebar-item>

      <template #footer>
        <vs-row justify="space-between">
          <vs-avatar badge-color="danger" badge-position="top-right" circle>
            <i class="bx bx-bell"></i>

            <template #badge> 28 </template>
          </vs-avatar>
          <vs-avatar history history-gradient circle>
            <img src="/kaneki.jpg" alt="" />
          </vs-avatar>
        </vs-row>
      </template>
    </vs-sidebar>
  </div>
</template>
<script>
export default {
  name: 'Sidebar',
  data: () => ({
    active: 'home',
    activeSidebar: false,
    isMobile: false,
    openSidebar: true,
  }),
  mounted() {
    this.isMobile = screen.width > 760 ? false : true
    if (!this.isMobile) {
      this.openSidebar = true
    } else {
      this.openSidebar = false
    }
  },
  methods: {
    openMenu() {
      this.activeSidebar = !this.activeSidebar
      this.openSidebar = true
    },
    closeMenu() {
      this.activeSidebar = !this.activeSidebar
      this.openSidebar = false
    },
  },
}
</script>
<style lang="scss" scoped>
$accentcolor: #ff6600;
.vs-sidebar-content.textWhite .vs-sidebar__item:after {
  background: $accentcolor !important;
}

.vs-sidebar__item__text {
  overflow: visible !important;
}
.vs-sidebar-content.textWhite .vs-sidebar__item.active {
  color: #ff6600 !important;
}
</style>
