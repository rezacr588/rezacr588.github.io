<script setup>
import CircledImageVueVue from "./CircledImageVue.vue";
import TypographyVue from "./main/TypographyVue.vue";
import SpaceVue from "./main/SpaceVue.vue";
import IconVue from "./main/IconVue.vue";
</script>

<template>
  <section>
    <CircledImageVueVue />
    <SpaceVue scope="block" size="16px" />
    <TypographyVue component="h4">Reza Zeraat</TypographyVue>
    <SpaceVue scope="block" size="8px" />
    <TypographyVue component="p">Software Developer</TypographyVue>
    <SpaceVue scope="block" size="8px" />
    <div class="row">
      <IconVue name="facebook" active="true"></IconVue>
      <SpaceVue scope="block" size="6px" />
      <IconVue name="instagram" active="true"></IconVue>
      <SpaceVue scope="block" size="6px" />
      <IconVue name="twitter" active="true"></IconVue>
      <SpaceVue scope="block" size="6px" />
      <IconVue name="linkedin" active="true"></IconVue>
      <SpaceVue scope="block" size="6px" />
      <IconVue name="youtube" active="true"></IconVue>
      <SpaceVue scope="block" size="6px" />
      <IconVue name="dribbble" active="true"></IconVue>
    </div>
    <hr />
    <div>
      <div class="item" v-for="data in items" :key="data.id">
        <div class="key">
          <TypographyVue component="p">{{ data.key + ":" }}</TypographyVue>
        </div>
        <div class="value">
          <TypographyVue component="p" color="data.color">{{
            data.value
          }}</TypographyVue>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  data: function () {
    return {
      items: [
        { id: 1, key: "Age", value: 25 },
        { id: 2, key: "Residence", value: "Turkey" },
        { id: 3, key: "Freelance", value: "Available", color: "#7EB942" },
        { id: 4, key: "Address", value: "Duzce, Konuralp" },
      ],
    };
  },
};
</script>

<style scoped>
section {
  background-color: white;
  text-align: center;
  display: flex;
  flex-direction: column;
  align-items: center;
  padding-top: 2rem;
}

.row {
  display: flex;
}
hr {
  width: 80%;
  height: 1px;
  background-color: #f0f0f6;
  border: none;
  margin: 1.5rem auto;
}
.key {
  background: #ffb400;
  padding: 3px;
}

.item {
  display: flex;
  justify-content: space-between;
  margin: 1rem 0;
}
</style>
