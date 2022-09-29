<script>
import RecommendationItem from "./RecommendationItem.vue";
export default {
  props: {
    recommendations: {
      type: Array,
      required: true,
    },
  },
  components: { RecommendationItem },
};
</script>
<template>
  <div class="container">
    <RecommendationItem
      v-for="recommendation in recommendations"
      :key="recommendation.opinion.title"
      :title="recommendation.opinion.title"
      :description="recommendation.opinion.description"
      :score="recommendation.opinion.score"
      :name="recommendation.name"
      :job="recommendation.jobTitle"
      :picture="recommendation.picture"
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
