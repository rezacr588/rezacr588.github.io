<script setup>
import { works } from "@/data/index.js";
import SectionBodyLayout from "../layouts/SectionBodyLayout.vue";
import HistoryLayout from "../layouts/HistoryLayout.vue";
</script>
<template>
  <SectionBodyLayout
    id="work"
    title="Work Experience"
    description="I have been working as a Web Developer for 6 years. These are a brief list of my work experiences."
  >
    <HistoryLayout :data="works" />
  </SectionBodyLayout>
</template>
