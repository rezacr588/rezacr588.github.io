<script setup>
import InformationsVue from "../components/InformationsVue.vue";
import NavbarVue from "../components/NavbarVue.vue";
import MainSections from "@/components/Sections/MainSections.vue";
</script>

<template>
  <main class="layout">
    <InformationsVue />
    <MainSections />
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
