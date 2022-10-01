<script setup>
import ServiceContainer from "./Services/ServiceContainer.vue";
import SectionBodyLayout from "../layouts/SectionBodyLayout.vue";
import { services } from "@/data";
</script>
<template>
  <SectionBodyLayout
    id="services"
    title="What I Offer"
    description="I can help you build a product, feature or website. Look through some of my expertise below."
  >
    <ServiceContainer :services="services" />
  </SectionBodyLayout>
</template>
