<script setup>
import TypographyVue from "./main/TypographyVue.vue";
import IconLink from "./icons/IconLink.vue";
import SpaceVue from "./main/SpaceVue.vue";
</script>
<template>
  <ul>
    <li :key="item.id" v-for="item in extraSkills">
      <IconLink /><SpaceVue scope="span" size="4px" /><TypographyVue
        component="p"
        color="#767676"
      >
        {{ item.text }}
      </TypographyVue>
    </li>
  </ul>
</template>
<script>
export default {
  props: {
    extraSkills: {
      type: Array,
      required: true,
    },
  },
};
</script>
<style scoped>
ul {
  list-style: none;
  padding: 0;
  text-align: left;
}
li {
  margin-bottom: 8px;
  display: flex;
  align-items: center;
}
</style>
