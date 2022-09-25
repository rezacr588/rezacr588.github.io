<script setup>
import SectionBodyLayout from "../main/SectionBodyLayout.vue";
import PricesContainer from "./Prices/PricesContainer.vue";

const prices = [
  {
    title: "front end developer",
    rate: "$20",
    popular: false,
    description:
      "This price is for companies that need a front end developer to build their website and web applicatons.",
    features: [
      { title: "react", checked: true },
      { title: "vue", checked: true },
      { title: "angular", checked: true },
      { title: "Next.js", checked: true },
      { title: "React Native", checked: true },
      { title: "Flutter", checked: true },
      { title: "Nuxt.js", checked: false },
      { title: "Swift", checked: false },
    ],
  },
  {
    title: "back end developer",
    rate: "$30",
    popular: false,
    description:
      "This price is for companies that need a front end developer to build their website and web applicatons.",
    features: [
      { title: "react", checked: true },
      { title: "vue", checked: true },
      { title: "angular", checked: true },
      { title: "Flutter", checked: true },
      { title: "Nuxt.js", checked: false },
      { title: "Swift", checked: false },
      { title: "Swift", checked: false },
    ],
  },
  {
    title: "full stack developer",
    rate: "$50",
    popular: true,
    description:
      "This price is for companies that need a front end developer to build their website and web applicatons.",
    features: [
      { title: "react", checked: true },
      { title: "vue", checked: true },
      { title: "angular", checked: true },
      { title: "React Native", checked: true },
      { title: "Flutter", checked: true },
      { title: "Nuxt.js", checked: false },
      { title: "Swift", checked: false },
    ],
  },
];
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
