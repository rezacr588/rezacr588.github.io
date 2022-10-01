<script setup>
import SectionBodyLayout from "../main/SectionBodyLayout.vue";
import HistoryLayout from "../main/HistoryLayout.vue";
import { educations } from "@/data/index.js";
</script>
<template>
  <SectionBodyLayout
    id="Education"
    title="Education"
    description="I have a Bachelor's degree in Biology Science from the University of Farhangian, Iran."
  >
    <HistoryLayout :data="educations" />
  </SectionBodyLayout>
</template>
