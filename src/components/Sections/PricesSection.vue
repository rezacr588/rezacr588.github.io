<script setup>
import { prices } from "@/data";
import PricesContainer from "./Prices/PricesContainer.vue";
import SectionBodyLayout from "../layouts/SectionBodyLayout.vue";
</script>

<template>
  <SectionBodyLayout
    id="price"
    title="Pay rate"
    description="My pay rate according to titles"
  >
    <PricesContainer :prices="prices" />
  </SectionBodyLayout>
</template>
