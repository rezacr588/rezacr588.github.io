<script setup>
import { reactive } from "vue";
import SectionBodyLayout from "../layouts/SectionBodyLayout.vue";
import TypographyVue from "../main/TypographyVue.vue";
const tabs = [
  { title: "All", active: true },
  { title: "Web", active: false },
  { title: "Mobile", active: false },
  { title: "Desktop", active: false },
];
const tabsState = reactive({
  tabs,
});
const setTabActive = (title) =>
  tabsState.tabs.forEach((tab) => {
    tab.active = tab.title === title;
  });
</script>
<template>
  <SectionBodyLayout
    id="portfolio"
    title="Portfolio"
    description="Here is some of my portfolios that have been published"
  >
    <div class="tabs-container">
      <button
        class="tab-button"
        v-on:click="setTabActive(tab.title)"
        :key="tab.title"
        v-for="tab in tabsState.tabs"
      >
        <TypographyVue
          component="h4"
          :color="tab.active ? '#FFB400' : '#2B2B2B'"
          >{{ tab.title }}</TypographyVue
        >
      </button>
    </div>
  </SectionBodyLayout>
</template>

<style scoped>
.tabs-container {
  display: flex;
  justify-content: center;
  align-items: center;
  gap: 2rem;
}
.tab-button {
  background-color: transparent;
  outline: none;
  border: none;
}
.tab-button:hover {
  cursor: pointer;
  color: #f9a826;
}
</style>
