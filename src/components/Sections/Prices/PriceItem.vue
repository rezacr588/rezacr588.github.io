<script setup>
import TypographyVue from "@/components/main/TypographyVue.vue";
import SpaceVue from "@/components/main/SpaceVue.vue";
const props = defineProps([
  "title",
  "rate",
  "popular",
  "description",
  "features",
]);
</script>
<template>
  <div class="item-container">
    <div class="popular-ticket" v-if="props.popular">
      <TypographyVue component="p">Most Popular</TypographyVue>
    </div>
    <SpaceVue />
    <TypographyVue component="h3">
      {{ props.title }}
    </TypographyVue>
    <SpaceVue />
    <div class="row">
      <TypographyVue component="h4">
        {{ props.rate }}
      </TypographyVue>
      <TypographyVue component="p"> /hour </TypographyVue>
    </div>
    <SpaceVue />
    <TypographyVue component="p" color="#767676">
      {{ props.description }}
    </TypographyVue>
    <SpaceVue />
    <ul>
      <li v-for="feature in props.features" :key="feature.title">
        <TypographyVue component="p" color="#767676">
          {{ feature.title }}
        </TypographyVue>
        <SpaceVue />
        <div class="checkmark" v-if="feature.checked">
          <svg
            width="14"
            height="14"
            viewBox="0 0 14 14"
            fill="none"
            xmlns="http://www.w3.org/2000/svg"
          >
            <path
              d="M5.66667 11.3333L2.66667 8.33333L1.33333 9.66667L5.66667 14L12.6667 7L11.3333 5.66667L5.66667 11.3333Z"
              fill="#FFB400"
            />
          </svg>
        </div>
        <div class="uncheck" v-else>
          <svg
            width="14"
            height="14"
            viewBox="0 0 14 14"
            fill="none"
            xmlns="http://www.w3.org/2000/svg"
          >
            <path
              d="M1.33333 7H12.6667M7 1.33333V12.6667"
              stroke="#767676"
              stroke-width="2"
              stroke-linecap="round"
              stroke-linejoin="round"
            />
          </svg>
        </div>
      </li>
    </ul>
  </div>
</template>

<style scoped>
.row {
  display: flex;
}
.popular-ticket {
  background: #ffb400;
  padding: 10px;
  border-radius: 5px;
  margin-bottom: 10px;
}
.item-container {
  background: #fff;
  border-radius: 10px;
  padding: 20px;
  box-shadow: 0px 0px 10px rgba(0, 0, 0, 0.1);
  margin: 0 10px;
}
</style>
