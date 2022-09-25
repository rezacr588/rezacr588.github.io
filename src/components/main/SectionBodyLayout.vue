<script setup>
import Typography from "../main/TypographyVue.vue";
import SpaceVue from "../main/SpaceVue.vue";

const props = defineProps(["id", "title", "description"]);
</script>
<template>
  <section :id="props.id">
    <Typography component="h2" color="#2B2B2B"> {{ props.title }} </Typography>
    <SpaceVue />
    <Typography component="p" color="#767676">
      {{ props.description }}
    </Typography>
    <SpaceVue size="1rem" />
    <slot></slot>
  </section>
</template>

<style scoped>
section {
  margin: 70px auto;
  text-align: center;
}
</style>
