<template>
  <h4 v-if="component === 'h4'">
    <slot></slot>
  </h4>
  <p v-if="component === 'p'">
    <slot></slot>
  </p>
</template>
<script>
export default {
  props: {
    component: {
      type: String,
    },
  },
};
</script>

<style scoped>
h4 {
  /* H4 - 18px */
  font-family: "Inter";
  font-style: normal;
  font-weight: 500;
  font-size: 18px;
  line-height: 123.6%;
  text-transform: capitalize;
  color: #2b2b2b;
}
p {
  /* Paragraph Progress - 15 */

  font-family: "Inter";
  font-style: normal;
  font-weight: 400;
  font-size: 15px;
  line-height: 24px;
  /* identical to box height, or 160% */

  text-transform: capitalize;
  font-feature-settings: "calt" off, "kern" off;

  /* Paragraph Font */

  color: #767676;
}
</style>
