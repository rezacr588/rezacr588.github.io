<script>
export default {
  props: {
    persons: {
      type: Array,
      required: true,
    },
  },
};
</script>
<template>
  <div class="container">
    <RecommendationItem
      v-for="person in persons"
      :key="person.opinion.title"
      :title="person.opinion.title"
      :description="person.opinion.description"
      :score="person.opinion.score"
      :name="person.name"
      :job="person.jobTitle"
      :picture="person.picture"
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
