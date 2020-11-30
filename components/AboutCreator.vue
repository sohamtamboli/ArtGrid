<template>
  <div>
    <div class="grid-container">
      <vs-avatar class="pfp" history history-gradient circle size="220">
        <img src="kaneki.jpg" alt="" />
      </vs-avatar>
      <div class="name-tag">
        <h1 class="name-title">Soham Tamboli</h1>
        <h4 class="subtext">Designer, Developer, Learner...</h4>
      </div>
      <div class="bio">
        <h3>About the creator:</h3>
        <p>
          Hi, I’m Soham! I’m a 21 years old youngster who loves Art! I wanted to
          make this webapp so that people like me can share their artworks. I
          had this idea in my mind for some time now and finally started working
          on it. :) Actually it started with project submission in college But
          now I think I’ll convert it into full working product!
        </p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'AboutCreator',
}
</script>

<style lang="scss" scoped>
.grid-container {
  display: grid;
  height: 100vh;
  grid-template-rows: 1fr 0.3fr 1fr;
  grid-template-areas:
    'avatar'
    'nametag'
    'info';
}

.pfp {
  grid-area: avatar;
  place-self: center;
}
.name-tag {
  grid-area: nametag;
  align-self: start;
  text-align: center;
}
.bio {
  grid-area: info;
  align-self: start;
  padding: 16px 32px;

  h3 {
    padding: 10px 0;
    color: #d8d8d8;
  }
  p {
    text-align: left;
    padding: 6px 0;
    line-height: 1.3;
    color: #a0a0a0;
  }
}
.vs-avatar-content.history--gradient:after {
  background-image: linear-gradient(
    45deg,
    #b92b27 33%,
    #1565c0 66%,
    #c471ed 99%
  ) !important;
}

@media only screen and (min-width: 600px) {
  .grid-container {
    display: grid;
    height: 100vh;
    grid-template-rows: 0.8fr 1fr;
    grid-template-columns: 0.8fr 2fr 2fr 0.8fr;
    grid-template-areas:
      '. avatar nametag .'
      '. info info .';
  }
  .pfp {
    grid-area: avatar;
    align-self: center;
    justify-self: center;
  }
  .name-tag {
    grid-area: nametag;
    align-self: center;
    justify-self: start;
    text-align: left;
  }
  .bio {
    grid-area: info;
    align-self: start;
    padding: 16px 32px;
  }
}
</style>
