<script setup>
import TypographyVue from "@/components/main/TypographyVue.vue";
import SpaceVue from "@/components/main/SpaceVue.vue";
defineProps({
  title: {
    type: String,
    required: true,
  },
  description: {
    type: String,
    required: true,
  },
  score: {
    type: Number,
    required: true,
  },
  name: {
    type: String,
    required: true,
  },
  job: {
    type: String,
    required: true,
  },
  picture: {
    type: String,
    required: true,
  },
});
</script>
<template>
  <div class="item">
    <div class="opinion">
      <div class="score">
        <svg
          v-for="i in score"
          :key="i"
          width="18"
          height="18"
          viewBox="0 0 18 18"
          fill="none"
          xmlns="http://www.w3.org/2000/svg"
        >
          <path
            d="M9 13.2448L12.9107 12.2343L14.5446 17.3684L9 13.2448ZM18 6.60873H11.1161L9 0L6.88393 6.60873H0L5.57143 10.7051L3.45535 17.3138L9.02679 13.2175L12.4554 10.7051L18 6.60873Z"
            fill="#FFB400"
          />
        </svg>
      </div>
      <SpaceVue />
      <TypographyVue component="h4">{{ title }}</TypographyVue>
      <SpaceVue />
      <TypographyVue component="p" color="#767676">{{
        description
      }}</TypographyVue>
    </div>
    <SpaceVue />
    <div class="person">
      <img class="person-img" :src="picture" alt="person" />
      <div>
        <TypographyVue component="h4">{{ name }}</TypographyVue>
        <TypographyVue component="p">{{ job }}</TypographyVue>
      </div>
    </div>
  </div>
</template>

<style scoped>
.item {
  background-color: white;
  padding: 25px;
  text-align: left;
}
.score {
  display: flex;
  gap: 5px;
}
.person-img {
  width: 80px;
  height: 80px;
  border-radius: 50%;
}
.person {
  display: flex;
  gap: 10px;
  align-items: center;
}
</style>
