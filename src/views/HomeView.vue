<script setup>
import HeaderVue from "../components/HeaderVue.vue";
import InformationsVue from "../components/InformationsVue.vue";
import NavbarVue from "../components/NavbarVue.vue";
</script>

<template>
  <main class="layout">
    <InformationsVue />
    <HeaderVue />
    <NavbarVue />
  </main>
</template>

<style scoped>
.layout {
  display: grid;
  grid-template-columns: 2fr 8fr 1fr;
  gap: 2rem;
}
</style>
