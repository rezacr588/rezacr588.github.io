<script setup>
import TypographyVue from "@/components/main/TypographyVue.vue";
import SpaceVue from "@/components/main/SpaceVue.vue";
import IconRemove from "@/components/icons/IconRemove.vue";
import IconChecked from "../../icons/IconChecked.vue";
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
          <IconChecked />
        </div>
        <div class="removed" v-else>
          <IconRemove />
        </div>
        <SpaceVue />
        <TypographyVue component="p" color="#767676">
          {{ feature.title }}
        </TypographyVue>
      </li>
    </ul>
    <SpaceVue />
    <button :class="`order-button ${props.popular ? 'active' : 'passive'}`">
      ORDER NOW
    </button>
    <SpaceVue />
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

.order-button {
  box-shadow: 0px 1px 10px rgba(0, 0, 0, 0.15);
  border-radius: 30px;
  font-family: "Inter";
  font-style: normal;
  font-weight: 700;
  font-size: 14px;
  line-height: 17px;
  text-transform: capitalize;
  color: #2b2b2b;
  outline: none;
  padding: 0.8rem 2rem;
  border: none;
  cursor: pointer;
}
.active {
  background: #ffb400;
}
.passive {
  background: #ffffff;
}
</style>
