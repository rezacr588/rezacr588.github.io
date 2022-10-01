<script setup>
import { recommendations } from "@/data";
import RecommendationsContainer from "./Recommandations/RecommendationsContainer.vue";
import SectionBodyLayout from "../layouts/SectionBodyLayout.vue";
</script>
<template>
  <SectionBodyLayout
    id="recommendations"
    title="Recommendations"
    description="In the years that I worked as a developer I have had the opportunity to work with many people. Here are some of the recommendations I have received."
  >
    <RecommendationsContainer :recommendations="recommendations" />
  </SectionBodyLayout>
</template>
