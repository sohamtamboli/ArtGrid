<template>
  <div>
    <div class="grid-container">
      <div class="profile-info">
        <vs-avatar
          class="profile--pfp"
          history
          history-gradient
          circle
          :size="size"
        >
          <img src="eren.jpg" alt="" />
        </vs-avatar>
        <div class="profile--name-tag">
          <h2 class="name-title">ArtxIntegrity</h2>
          <h4 class="subtext">3D Artist, Illustrator</h4>
        </div>
      </div>
      <div class="btn">Add Post Button</div>
      <ImageGrid class="posts" />
    </div>
  </div>
</template>

<script>
import ImageGrid from '@/components/ImageGrid'
export default {
  name: 'ProfileTest',
  components: {
    ImageGrid,
  },
  data() {
    return {
      isMobile: '',
      size: '',
    }
  },
  mounted() {
    this.isMobile = screen.width > 760 ? false : true
    if (this.isMobile) {
      this.size = '110'
    } else {
      this.size = '220'
    }
  },
}
</script>

<style lang="scss" scoped>
.vs-avatar-content.history--gradient[data-v-64be198c]:after {
  background-image: linear-gradient(
    45deg,
    #b92b27 33%,
    #1565c0 66%,
    #c471ed 99%
  ) !important;
}
.grid-container {
  display: grid;
  height: 100vh;
  grid-template-rows: 0.3fr 0.2fr 1fr;
  grid-template-areas:
    'profileInfo'
    'addBtn'
    'imgs';
}
.profile-info {
  display: flex;
  align-items: center;
  justify-content: space-evenly;
  grid-area: profileInfo;
  padding: 2em 0;

  .profile--name-tag {
    align-self: center;
  }
}

.btn {
  grid-area: addBtn;
  place-self: left;
}

.posts {
  grid-area: imgs;
  margin: 0 auto;
}

@media only screen and (min-width: 600px) {
  .grid-container {
    display: grid;
    height: 100vh;
    grid-template-rows: 0.5fr 0.2fr 1fr;
    grid-template-columns: 0.6fr 2fr 2fr 0.6fr;
    grid-template-areas:
      '. profileInfo profileInfo .'
      '. addBtn . .'
      '. imgs imgs .';
  }
  .profile-info {
    display: flex;
    flex-flow: column;
    align-items: center;
    justify-content: space-evenly;
    grid-area: profileInfo;
    padding: 2em 0;

    .profile--name-tag {
      align-self: center;
      padding: 2em 1em;
      text-align: center;
      h2 {
        font-size: 2em;
      }
    }
  }
  .posts {
    grid-area: imgs;
    margin: 0;
    display: grid;
    gap: 3em;
    grid-template-columns: repeat(auto-fit, minmax(240px, 1fr));
  }
}
</style>
