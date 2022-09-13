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
    color: {
      type: String,
      default: "#2B2B2B",
    },
  },
  data() {
    return {
      colored: this.init_color,
    };
  },
  computed: {
    cssVar() {
      console.log(this.colored);
      return {
        /* variables you want to pass to css */ "--color": this.colored,
      };
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
  color: var(--color);
}
p {
  /* Paragraph Progress - 15 */

  font-family: "Inter";
  font-style: normal;
  font-weight: 400;
  font-size: 15px;
  line-height: 24px;
  text-transform: capitalize;
  font-feature-settings: "calt" off, "kern" off;
  color: var(--color);
}
</style>
