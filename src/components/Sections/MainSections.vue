<script setup>
import HeaderVue from "../HeaderVue.vue";
import PricesSection from "./PricesSection.vue";
import ServicesSection from "./ServicesSection.vue";
import RecommendationsSection from "./RecommendationsSection.vue";
import EducationSection from "./EducationSection.vue";
import WorkSection from "./WorkSection.vue";
import PortfolioSection from "./PortfolioSection.vue";
</script>
<template>
  <main>
    <HeaderVue />
    <ServicesSection />
    <PricesSection />
    <RecommendationsSection />
    <EducationSection />
    <WorkSection />
    <PortfolioSection />
  </main>
</template>
