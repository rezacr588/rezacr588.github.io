<template>
  <h1 v-if="component === 'h1'">
    <slot></slot>
  </h1>
  <h2 v-else-if="component === 'h2'">
    <slot></slot>
  </h2>
  <h3 v-else-if="component === 'h3'">
    <slot></slot>
  </h3>
  <h4 v-else-if="component === 'h4'">
    <slot></slot>
  </h4>
  <h5 v-else-if="component === 'h5'">
    <slot></slot>
  </h5>
  <h6 v-else-if="component === 'h6'">
    <slot></slot>
  </h6>
  <p v-else-if="component === 'p'">
    <slot></slot>
  </p>
  <span v-else>
    <slot></slot>
  </span>
</template>
<script>
export default {
  props: {
    component: {
      type: String,
      required: true,
    },
    color: {
      type: String,
      default: "#2B2B2B",
    },
  },
};
</script>

<style scoped>
h1 {
  font-family: "Inter";
  font-style: normal;
  font-weight: 700;
  font-size: 35px;
  line-height: 123.6%;
  color: v-bind(color);
}
h3 {
  font-family: "Inter";
  font-style: normal;
  font-weight: 600;
  font-size: 24px;
  line-height: 123.6%;
  text-transform: capitalize;
  color: v-bind(color);
}
span {
  font-family: "Inter";
  font-style: normal;
  font-weight: 700;
  font-size: 35px;
  line-height: 123.6%;
  color: v-bind(color);
}
h2 {
  font-family: "Inter";
  font-style: normal;
  font-weight: 700;
  font-size: 32px;
  line-height: 123.6%;
  text-transform: capitalize;
  color: v-bind(color);
}
h4 {
  font-family: "Inter";
  font-style: normal;
  font-weight: 500;
  font-size: 18px;
  line-height: 123.6%;
  text-transform: capitalize;
  color: v-bind(color);
}
p {
  font-family: "Inter";
  font-style: normal;
  font-weight: 400;
  font-size: 15px;
  line-height: 24px;
  text-transform: capitalize;
  font-feature-settings: "calt" off, "kern" off;
  color: v-bind(color);
}
h6 {
  font-family: "Inter";
  font-style: normal;
  font-weight: 400;
  font-size: 14px;
  line-height: 20px;
  text-transform: capitalize;
  font-feature-settings: "calt" off, "kern" off;
  color: v-bind(color);
}
h5 {
  font-family: "Inter";
  font-style: normal;
  font-weight: 500;
  font-size: 12px;
  line-height: 15px;
  color: v-bind(color);
}
</style>
