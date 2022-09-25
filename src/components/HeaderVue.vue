<script setup>
import ButtonVue from "./main/ButtonVue.vue";
import IconVue from "./main/IconVue.vue";
import TypographyVue from "./main/TypographyVue.vue";
</script>

<template>
  <section id="home" class="container">
    <div class="left">
      <TypographyVue component="h1">
        I’m Reza Zeraat <br />
        <TypographyVue component="span">Full Stack</TypographyVue> Developer
      </TypographyVue>
      <TypographyVue component="h6">
        I am a hard working and ambitious man that loves to experience new
        adventures, one of my greatest passions was Application Programming,
        producing functional and appealing web applications on the internet.
      </TypographyVue>
      <ButtonVue>
        <TypographyVue component="h4"> HIRE ME </TypographyVue>
        <IconVue name="streightFlash" active="true"></IconVue>
      </ButtonVue>
    </div>
    <div class="right">
      <img src="../assets/header.jpeg" />
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
