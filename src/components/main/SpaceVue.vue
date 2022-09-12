<template>
  <div v-if="scope === 'block'"></div>
  <span v-else-if="scope === 'span'"></span>
</template>

<script>
export default {
  props: {
    size: {
      type: String,
    },
    scope: {
      type: String,
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
