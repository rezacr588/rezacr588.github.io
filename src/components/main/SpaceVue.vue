<template>
  <div v-if="scope === 'block'"></div>
  <span v-else-if="scope === 'span'"></span>
</template>

<script>
export default {
  props: {
    size: {
      type: String,
      default: ".5rem",
    },
    scope: {
      type: String,
      default: "block",
    },
  },
};
</script>
<style scoped>
div {
  padding: v-bind(size);
}
span {
  padding: v-bind(size);
}
</style>
