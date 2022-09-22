<script setup>
import IconContrastVue from "./icons/IconContrast.vue";
import SpaceVue from "./main/SpaceVue.vue";
import IconButton from "./main/IconButton.vue";
import TypographyVue from "./main/TypographyVue.vue";
</script>
<template>
  <section class="container">
    <div id="first">
      <IconContrastVue />
    </div>
    <div id="second">
      <div :key="button.name" v-for="button in buttons">
        <IconButton :icon="button.icon">
          <template #pop-up>
            <TypographyVue component="h5" color="white">
              {{ button.name }}
            </TypographyVue>
          </template>
        </IconButton>
        <SpaceVue />
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "NavbarVue",
  data: function () {
    return {
      buttons: [
        {
          name: "Home",
          icon: "Home",
        },
        {
          name: "Services",
          icon: "Services",
        },
        {
          name: "Edu",
          icon: "Edu",
        },
        {
          name: "Portfolio",
          icon: "Portfolio",
        },
        {
          name: "Contact",
          icon: "Contact",
        },
        {
          name: "Blog",
          icon: "Blog",
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
