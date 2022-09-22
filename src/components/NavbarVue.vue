<script setup>
import IconContrastVue from "./icons/IconContrast.vue";
import IconVue from "./main/IconVue.vue";
</script>
<template>
  <section class="container">
    <div id="first">
      <IconContrastVue />
    </div>
    <IconVue size="40px" name="Home" active="true"></IconVue>
    <IconVue size="40px" name="Services"></IconVue>
    <IconVue size="40px" name="Edu"></IconVue>
    <IconVue size="40px" name="Portfolio"></IconVue>
    <IconVue size="40px" name="Contact"></IconVue>
    <IconVue size="40px" name="Blog"></IconVue>
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
  display: flex;
}
#first {
  justify-self: flex-start;
}
</style>
