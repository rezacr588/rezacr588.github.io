<script>
import PriceItem from "./PriceItem.vue";
export default {
  props: {
    prices: {
      type: Array,
      required: true,
    },
  },
  components: { PriceItem },
};
</script>

<template>
  <div class="container">
    <PriceItem
      v-for="price in prices"
      :key="price.title"
      :title="price.title"
      :rate="price.rate"
      :popular="price.popular"
      :description="price.description"
      :features="price.features"
    />
  </div>
</template>

<style scoped>
.container {
  display: grid;
  grid-template-columns: 1fr 1fr 1fr;
  gap: 20px;
}
</style>
