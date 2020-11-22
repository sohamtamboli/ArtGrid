<template>
  <div class="hidden">
    <vs-navbar
      shadow
      color="#212121"
      text-white
      center-collapsed
      v-model="active"
    >
      <template #right>
        <vs-button flat circle color="#ff6600" size="large">Login</vs-button>
      </template>
    </vs-navbar>
    <vs-sidebar
      absolute
      v-model="active"
      hover-expand
      reduce
      open
      background="#212121"
      textWhite
    >
      <template #logo>
        <!-- ...img logo -->
      </template>
      <vs-sidebar-item id="home">
        <template #icon>
          <i class="bx bx-home"></i>
        </template>

        Home
      </vs-sidebar-item>

      <vs-sidebar-item id="Music">
        <template #icon>
          <i class="bx bxs-music"></i>
        </template>

        Music
      </vs-sidebar-item>
      <vs-sidebar-group>
        <template #header>
          <vs-sidebar-item arrow>
            <template #icon>
              <i class="bx bx-group"></i>
            </template>
            Social media
          </vs-sidebar-item>
        </template>

        <vs-sidebar-item id="Instagram">
          <template #icon>
            <i class="bx bxl-instagram"></i>
          </template>
          Instagram
        </vs-sidebar-item>
        <vs-sidebar-item id="twitter">
          <template #icon>
            <i class="bx bxl-twitter"></i>
          </template>
          Twitter
        </vs-sidebar-item>
        <vs-sidebar-item id="Facebook">
          <template #icon>
            <i class="bx bxl-facebook"></i>
          </template>
          Facebook
        </vs-sidebar-item>
      </vs-sidebar-group>
      <vs-sidebar-group>
        <template #header>
          <vs-sidebar-item arrow>
            <template #icon>
              <i class="bx bx-code-alt"></i>
            </template>
            Coding
          </vs-sidebar-item>
        </template>

        <vs-sidebar-item id="github">
          <template #icon>
            <i class="bx bxl-github"></i>
          </template>
          Github
        </vs-sidebar-item>

        <vs-sidebar-item id="discord">
          <template #icon>
            <i class="bx bxl-discord"></i>
          </template>
          Discord
        </vs-sidebar-item>

        <vs-sidebar-item id="git">
          <template #icon>
            <i class="bx bxl-git"></i>
          </template>
          Git
        </vs-sidebar-item>
      </vs-sidebar-group>

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
  }),
}
</script>
<style lang="css" scoped>
.vs-sidebar-content.textWhite .vs-sidebar__item:after {
  background: #ff6600 !important;
}
.vs-navbar-content.textWhite .vs-navbar__line {
  background: #ff6600 !important;
}
</style>
