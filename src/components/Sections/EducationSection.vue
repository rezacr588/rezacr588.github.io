<script setup>
import { educations } from "@/data/index.js";
import SectionBodyLayout from "../layouts/SectionBodyLayout.vue";
import HistoryLayout from "../layouts/HistoryLayout.vue";
</script>
<template>
  <SectionBodyLayout
    id="education"
    title="Education"
    description="I have a Bachelor's degree in Biology Science from the University of Farhangian, Iran."
  >
    <HistoryLayout :data="educations" />
  </SectionBodyLayout>
</template>
