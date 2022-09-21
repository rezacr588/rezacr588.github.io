<template>
  <h4 v-if="component === 'h4'">
    <slot></slot>
  </h4>
  <h1 v-if="component === 'h1'">
    <slot></slot>
  </h1>
  <p v-if="component === 'p'">
    <slot></slot>
  </p>
  <h6 v-if="component === 'h6'">
    <slot></slot>
  </h6>
</template>
<script>
export default {
  props: {
    component: {
      type: String,
    },
    color: {
      type: String,
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
  color: #2b2b2b;
}
h1 > span {
  color: #ffb400;
  font-family: "Inter";
  font-style: normal;
  font-weight: 700;
  font-size: 35px;
  line-height: 123.6%;
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
  color: #767676;
}
</style>
