<script setup>
import TypographyVueVue from "./TypographyVue.vue";
import SpaceVue from "./SpaceVue.vue";
</script>
<template>
  <div class="container">
    <TypographyVueVue component="h4">{{ title }}</TypographyVueVue>
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
