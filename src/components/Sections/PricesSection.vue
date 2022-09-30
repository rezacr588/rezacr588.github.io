<script setup>
import { prices } from "@/data";
import SectionBodyLayout from "../main/SectionBodyLayout.vue";
import PricesContainer from "./Prices/PricesContainer.vue";
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
