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
      <TypographyVue component="h2">
        {{ props.rate }}
      </TypographyVue>
      <TypographyVue component="p"> /hour </TypographyVue>
    </div>
    <SpaceVue />
    <div class="row">
      <SpaceVue />
      <TypographyVue component="p" color="#767676">
        {{ props.description }}
      </TypographyVue>
      <SpaceVue />
    </div>
    <SpaceVue />
    <ul class="list">
      <li
        class="list-item"
        v-for="feature in props.features"
        :key="feature.title"
      >
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
        <div class="removed" v-else>
          <svg
            width="14"
            height="14"
            viewBox="0 0 14 14"
            fill="none"
            xmlns="http://www.w3.org/2000/svg"
          >
            <path
              d="M1.33333 1.33333L12.6667 12.6667M12.6667 1.33333L1.33333 12.6667"
              stroke="#767676"
            />
          </svg>
        </div>
        <SpaceVue />
        <TypographyVue component="p" color="#767676">
          {{ feature.title }}
        </TypographyVue>
      </li>
    </ul>
  </div>
</template>

<style scoped>
.row {
  display: flex;
  justify-content: center;
  align-items: baseline;
}
.popular-ticket {
  background: #ffb400;
  padding: 10px;
  margin-bottom: 10px;
}
.item-container {
  background: #fff;
  text-align: center;
  box-shadow: 0px 0px 10px rgba(0, 0, 0, 0.1);
}
.list {
  list-style: none;
  padding: 0;
  margin: 0;
}
.list-item {
  display: flex;
  align-items: center;
  padding: 10px 0;
}
</style>
