<script setup>
import TypographyVue from "../main/TypographyVue.vue";
import SpaceVue from "../main/SpaceVue.vue";
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
      <div class="left-side">
        <TypographyVue component="h4" color="#2B2B2B">
          {{ item.place }}
        </TypographyVue>
        <SpaceVue />
        <div class="row">
          <TypographyVue component="p" color="#2B2B2B">
            {{ item.location }}
          </TypographyVue>
          <div class="date">{{ item.date }}</div>
        </div>
      </div>
      <div class="right-side">
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
.left-side {
  display: flex;
  flex-direction: column;
  align-items: flex-start;
}
.right-side {
  display: flex;
  flex-direction: column;
  align-items: flex-start;
  text-align: left;
  justify-content: space-between;
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
  color: #ffffff;
}
.row {
  display: flex;
  align-items: center;
}
</style>
