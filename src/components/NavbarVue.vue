<script setup>
import IconContrastVue from "./icons/IconContrast.vue";
import SpaceVue from "./main/SpaceVue.vue";
import IconButton from "./main/IconButton.vue";
import TypographyVue from "./main/TypographyVue.vue";
</script>
<template>
  <nav class="container">
    <div id="first">
      <IconContrastVue />
    </div>
    <div id="second">
      <div :key="button.name" v-for="button in buttons">
        <IconButton @click="goto(button.ref)" :icon="button.icon">
          <template #pop-up>
            <TypographyVue component="h5" color="white">
              {{ button.name }}
            </TypographyVue>
          </template>
        </IconButton>
        <SpaceVue />
      </div>
    </div>
  </nav>
</template>

<script>
export default {
  name: "NavbarVue",
  methods: {
    goto(id) {
      document.getElementById(id).scrollIntoView({
        behavior: "smooth",
      });
    },
  },
  data: function () {
    return {
      buttons: [
        {
          name: "Home",
          icon: "Home",
          ref: "home",
        },
        {
          name: "Services",
          icon: "Services",
          ref: "services",
        },
        {
          name: "Education",
          icon: "Edu",
          ref: "education",
        },
        {
          name: "Portfolio",
          icon: "Portfolio",
          ref: "portfolio",
        },
        {
          name: "Contact",
          icon: "Contact",
          ref: "contact",
        },
        {
          name: "Blog",
          icon: "Blog",
          ref: "blog",
        },
      ],
    };
  },
};
</script>

<style scoped>
.container {
  align-items: center;
  justify-content: center;
  height: 100vh;
  background-color: #fff;
  position: fixed;
  right: 0;
  grid-template-rows: 1fr 4fr;
  width: 120px;
  top: 0;
  display: grid;
}
#first {
  display: flex;
  justify-content: center;
  align-items: center;
}
#second {
  display: flex;
  flex-direction: column;
  justify-content: space-evenly;
  align-items: center;
}
</style>
