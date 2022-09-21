<script setup>
import ButtonVue from "./main/ButtonVue.vue";
import IconVue from "./main/IconVue.vue";
</script>

<template>
  <section class="container">
    <div class="left">
      <h1 class="title">
        I’m Reza Zeraat <br />
        <span>Full Stack</span> Developer
      </h1>
      <h6 class="description">
        I am a hard working and ambitious man that loves to experience new
        adventures, one of my greatest passions was Application Programming,
        producing functional and appealing web applications on the internet.
        When I didn't know anything about programming I always ask myself how
        could I make this app better and astonishing
      </h6>
      <ButtonVue title="HIRE ME">
        <IconVue name="streightFlash" active="true"></IconVue>
      </ButtonVue>
    </div>
    <div class="right">
      <img src="../assets/profile-image.png" />
    </div>
  </section>
</template>

<style scoped>
.container {
  background-image: url("../assets/headar-background.png");
  display: grid;
  flex: 1;
  grid-template-columns: 3fr 1fr;
  padding: 0 3rem;
  height: fit-content;
}
.title {
  font-family: "Inter";
  font-style: normal;
  font-weight: 700;
  font-size: 35px;
  line-height: 123.6%;
  color: #2b2b2b;
}
.title > span {
  color: #ffb400;
  font-family: "Inter";
  font-style: normal;
  font-weight: 700;
  font-size: 35px;
  line-height: 123.6%;
}

.description {
  /* H6 - 16px */

  font-family: "Inter";
  font-style: normal;
  font-weight: 400;
  font-size: 14px;
  line-height: 20px;
  /* or 150% */

  text-transform: capitalize;
  font-feature-settings: "calt" off, "kern" off;

  /* Paragraph Font */

  color: #767676;
}

.left {
  height: 100%;
  display: flex;
  flex-direction: column;
  justify-content: space-around;
  padding: 1rem;
}

.right > img {
  height: 60vh;
}
</style>
