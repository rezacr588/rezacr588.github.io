<script setup>
import TypographyVue from "./TypographyVue.vue";
import SpaceVue from "./SpaceVue.vue";
defineProps({
  data: {
    type: Array,
    required: true,
  },
});
</script>
<template>
  <ul class="list">
    <li :key="item.id" v-for="item in data" class="list-item">
      <div>
        <TypographyVue component="h4" color="#2B2B2B">
          {{ item.place }}
        </TypographyVue>
        <div class="row">
          <TypographyVue component="p" color="#2B2B2B">
            {{ item.location }}
          </TypographyVue>
          <div class="date">{{ item.date }}</div>
        </div>
      </div>
      <div>
        <TypographyVue component="h4" color="#2B2B2B">
          {{ item.title }}
        </TypographyVue>
        <SpaceVue />
        <TypographyVue component="p" color="#767676">
          {{ item.description }}
        </TypographyVue>
      </div>
    </li>
  </ul>
</template>
<style scoped>
.list {
  list-style: none;
  padding: 0;
  margin: 0;
  background-color: white;
  padding: 2rem;
}
.list-item {
  display: grid;
  grid-template-columns: 1fr 2fr;
  padding-bottom: 2rem;
  margin-top: 1.5rem;
  border-bottom: 1.5px solid #f0f0f6;
}
.list-item:last-child {
  border-bottom: none;
}
.date {
  background: #ffb400;
  border-radius: 1px;
  padding: 4px 7px;
  font-family: "Inter";
  font-style: normal;
  font-weight: 400;
  font-size: 10px;
  line-height: 100.9%;
  /* identical to box height, or 10px */

  /* White */

  color: #ffffff;
}
.row {
  display: flex;
  align-items: center;
}
</style>
