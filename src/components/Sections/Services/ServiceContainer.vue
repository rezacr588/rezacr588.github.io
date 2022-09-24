<script>
import Service from "./Service.vue";
export default {
  props: {
    services: {
      type: Array,
      required: true,
    },
  },
  components: { Service },
};
</script>

<template>
  <div class="container">
    <Service
      v-for="service in services"
      :key="service.title"
      :title="service.title"
      :description="service.description"
      :icon="service.icon"
    />
  </div>
</template>

<style scoped>
.container {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
  gap: 20px;
}
</style>
