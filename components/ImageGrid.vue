<template>
  <div>
    <vs-card class="card" type="5" v-for="(post, index) in posts" :key="index">
      <template #title>
        <h3>{{ post.title }}</h3>
      </template>
      <template #img>
        <img :src="post.img" alt="" />
      </template>
      <template #text>
        <p>{{ post.info }}</p>
      </template>
    </vs-card>
  </div>
</template>

<script>
export default {
  name: 'ImageGrid',
  data() {
    return {
      posts: [
        {
          title: 'Enlightened Forest Gate',
          img: 'artxintegrity/one.png',
          info: 'The silent night forest open up a Gate to Enlightenment!',
        },
        {
          title: 'Into The Space',
          img: 'artxintegrity/four.jpg',
          info: 'Distant planet in the deep space.',
        },
        {
          title: 'Lake of Clouds',
          img: 'artxintegrity/five.jpg',
          info: 'A calming lake of clouds!',
        },
        {
          title: 'Trapped Life',
          img: 'artxintegrity/two.png',
          info: "Earth's been preserved as an Antique Piece.",
        },
        {
          title: 'Balance House',
          img: 'artxintegrity/three.png',
          info: 'Perfectly Balanced as all things should be!',
        },
      ],
    }
  },
}
</script>

<style lang="scss" scoped>
.card {
  margin: 2em 0;
}
.vs-card-content.type-5 .vs-card {
  background: inherit !important;
}
</style>
