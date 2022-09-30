<script>
import RecommendationItem from "./RecommendationItem.vue";
export default {
  props: {
    recommendations: {
      type: Array,
      required: true,
    },
  },
  data() {
    return {
      items: this.recommendations,
      current: 1,
    };
  },
  components: { RecommendationItem },
  computed: {
    dotsCount() {
      return Math.ceil(this.recommendations.length / 3);
    },
    showedItems() {
      return this.items.slice((this.current - 1) * 3, this.current * 3);
    },
  },
  methods: {
    next() {
      if (this.current < this.dotsCount - 1) {
        this.current++;
      }
    },
    prev() {
      if (this.current > 0) {
        this.current--;
      }
    },
    goTo(index) {
      this.current = index;
    },
  },
};
</script>
<template>
  <div class="container">
    <RecommendationItem
      v-for="recommendation in showedItems"
      :key="recommendation.opinion.title"
      :title="recommendation.opinion.title"
      :description="recommendation.opinion.description"
      :score="recommendation.opinion.score"
      :name="recommendation.name"
      :job="recommendation.jobTitle"
      :picture="recommendation.picture"
    />
  </div>
  <div class="dot-container">
    <div :key="i" v-for="i in dotsCount" class="dot" v-on:click="goTo(i)" />
  </div>
</template>

<style scoped>
.container {
  display: grid;
  grid-template-columns: 1fr 1fr 1fr;
  gap: 20px;
}
.dot-container {
  display: flex;
  justify-content: center;
  margin-top: 20px;
}
.dot {
  width: 10px;
  height: 10px;
  border-radius: 50%;
  background-color: #ffb400;
}
</style>
