<script setup>
import TypographyVue from "./main/TypographyVue.vue";
import SpaceVue from "./main/SpaceVue.vue";
</script>
<template>
  <div class="container">
    <TypographyVue component="h4">{{ title }}</TypographyVue>
    <SpaceVue scope="block" size="8px" />
    <div :key="item.id" v-for="item in list" class="item-container">
      <div class="label">
        <TypographyVue component="p" color="#767676">
          {{ item.key }}
        </TypographyVue>
        <TypographyVue component="p" color="#767676">
          {{ item.value }}%
        </TypographyVue>
      </div>
      <div class="progress">
        <div class="progress-bar" :style="`width: ${item.value}%`"></div>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  props: {
    list: {
      type: Array,
    },
    color: {
      type: String,
    },
    title: {
      type: String,
    },
  },
};
</script>
<style scoped>
.container {
  padding: 16px;
  width: 100%;
  display: flex;
  flex-direction: column;
  align-items: baseline;
}

.item-container {
  width: 100%;
  margin: 0.3rem 0;
}
.label {
  display: flex;
  justify-content: space-between;
  width: 100%;
}
.progress {
  width: 100%;
  height: 4px;
  margin-top: 4px;
  background-color: #fff;
  border-radius: 30px;
  padding: 1px;
  outline: #ffb400 1px solid;
  position: relative;
}
.progress-bar {
  height: 100%;
  background-color: #ffb400;
  border-radius: 30px;
  position: relative;
  transition: width 0.5s ease;
}
.progress-label {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  display: flex;
  align-items: center;
  justify-content: center;
  color: white;
}
</style>
