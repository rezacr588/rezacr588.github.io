<script setup>
import IconContrastVue from "./icons/IconContrast.vue";
import SpaceVue from "./main/SpaceVue.vue";
</script>
<template>
  <section class="container">
    <SpaceVue scope="block" size="50px" />
    <IconContrastVue />
    <SpaceVue scope="block" size="50px" />
  </section>
</template>

<style scoped>
.container {
  display: flex;
  flex-direction: column;
  align-items: center;
  height: 100%;
  width: 100%;
  background-color: #fff;
}
</style>
