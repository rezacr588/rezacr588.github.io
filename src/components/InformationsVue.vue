<script setup>
import CircledImageVueVue from "./CircledImageVue.vue";
import TypographyVue from "./main/TypographyVue.vue";
import SpaceVue from "./main/SpaceVue.vue";
import IconVue from "./main/IconVue.vue";
</script>

<template>
  <section>
    <CircledImageVueVue />
    <SpaceVue scope="block" size="16px" />
    <TypographyVue component="h4">Reza Zeraat</TypographyVue>
    <SpaceVue scope="block" size="8px" />
    <TypographyVue component="p">Software Developer</TypographyVue>
    <SpaceVue scope="block" size="8px" />
    <div class="row">
      <IconVue name="facebook" active="true"></IconVue>
      <SpaceVue scope="block" size="6px" />
      <IconVue name="instagram" active="true"></IconVue>
      <SpaceVue scope="block" size="6px" />
      <IconVue name="twitter" active="true"></IconVue>
      <SpaceVue scope="block" size="6px" />
      <IconVue name="linkedin" active="true"></IconVue>
      <SpaceVue scope="block" size="6px" />
      <IconVue name="youtube" active="true"></IconVue>
      <SpaceVue scope="block" size="6px" />
      <IconVue name="dribbble" active="true"></IconVue>
    </div>
  </section>
</template>

<style scoped>
section {
  background-color: white;
  text-align: center;
  display: flex;
  flex-direction: column;
  align-items: center;
  padding-top: 2rem;
}
.row {
  display: flex;
}
</style>
