<script setup>
import CircledImageVueVue from "./CircledImageVue.vue";
import TypographyVue from "./main/TypographyVue.vue";
import SpaceVue from "./main/SpaceVue.vue";
</script>

<template>
  <section>
    <CircledImageVueVue />
    <SpaceVue scope="block" size="16px" />
    <TypographyVue component="h4">Reza Zeraat</TypographyVue>
    <SpaceVue scope="block" size="8px" />
    <TypographyVue component="p">Software Developer</TypographyVue>
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
</style>
