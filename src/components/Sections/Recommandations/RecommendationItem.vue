<script setup>
defineProps({
  title: {
    type: String,
    required: true,
  },
  description: {
    type: String,
    required: true,
  },
  score: {
    type: Number,
    required: true,
  },
  name: {
    type: String,
    required: true,
  },
  job: {
    type: String,
    required: true,
  },
  picture: {
    type: String,
    required: true,
  },
});
</script>
<template>
  <div class="container">
    <div class="opinion">
      <h3>{{ title }}</h3>
      <p>{{ description }}</p>
      <div class="score">
        <span class="score__value">{{ score }}</span>
        <span class="score__max">/5</span>
      </div>
    </div>
    <div class="person">
      <h4>{{ name }}</h4>
      <p>{{ job }}</p>
    </div>
  </div>
</template>

<style scoped></style>
