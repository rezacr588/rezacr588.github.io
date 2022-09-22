<script setup>
import IconContrastVue from "./icons/IconContrast.vue";
import IconVue from "./main/IconVue.vue";
import SpaceVue from "./main/SpaceVue.vue";
</script>
<template>
  <section class="container">
    <div id="first">
      <IconContrastVue />
    </div>
    <div id="second">
      <IconVue size="40px" name="Home" active="true"></IconVue>
      <SpaceVue />
      <IconVue size="40px" name="Services"></IconVue>
      <SpaceVue />
      <IconVue size="40px" name="Edu"></IconVue>
      <SpaceVue />
      <IconVue size="40px" name="Portfolio"></IconVue>
      <SpaceVue />
      <IconVue size="40px" name="Contact"></IconVue>
      <SpaceVue />
      <IconVue size="40px" name="Blog"></IconVue>
    </div>
  </section>
</template>

<style scoped>
.container {
  align-items: center;
  justify-content: center;
  height: 100vh;
  background-color: #fff;
  position: fixed;
  right: 0;
  grid-template-rows: 1fr 4fr;
  width: 120px;
  top: 0;
  display: grid;
}
#first {
  display: flex;
  justify-content: center;
  align-items: center;
}
#second {
  display: flex;
  flex-direction: column;
  justify-content: space-evenly;
  align-items: center;
}
</style>
