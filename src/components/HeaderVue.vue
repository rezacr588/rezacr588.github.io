<script setup>
import ButtonVue from "./main/ButtonVue.vue";
import IconVue from "./main/IconVue.vue";
</script>

<template>
  <div class="container">
    <div class="left">
      <h1 class="title">I’m Reza Zeraat <span>Software</span> Developer</h1>
      <h6 class="description">
        Lorem ipsum dolor sit amet, consectetur adipiscing elit. Et, volutpat
        feugiat placerat lobortis. Natoque rutrum semper sed suspendisse nunc
        lectus.
      </h6>
      <ButtonVue title="HIRE ME">
        <IconVue name="streightFlash"></IconVue>
      </ButtonVue>
    </div>
    <div class="right">
      <img src="../assets/profile-image.png" />
    </div>
  </div>
</template>

<style scoped>
.container {
  background-image: url("../assets/headar-background.png");
  display: grid;
  flex: 1;
  grid-template-columns: 3fr 1fr;
  width: 70%;
  padding: 0 3rem;
}
.title {
  font-family: "Inter";
  font-style: normal;
  font-weight: 700;
  font-size: 48px;
  line-height: 123.6%;
  color: #2b2b2b;
}
.title > span {
  color: #ffb400;
  font-family: "Inter";
  font-style: normal;
  font-weight: 700;
  font-size: 48px;
  line-height: 123.6%;
}

.description {
  /* H6 - 16px */

  font-family: "Inter";
  font-style: normal;
  font-weight: 400;
  font-size: 16px;
  line-height: 24px;
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
