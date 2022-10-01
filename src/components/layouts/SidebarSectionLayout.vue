<script setup>
import TypographyVue from "../main/TypographyVue.vue";
import SpaceVue from "../main/SpaceVue.vue";
</script>
<template>
  <div class="container">
    <TypographyVue component="h4">{{ title }}</TypographyVue>
    <SpaceVue scope="block" size="4px" />
    <slot></slot>
  </div>
</template>
<script>
export default {
  props: {
    title: {
      type: String,
    },
  },
};
</script>
<style scoped>
.container {
  padding: 0 16px;
  width: 100%;
  display: flex;
  flex-direction: column;
  align-items: baseline;
}
</style>
