<script>
import WebDevelopmentIcon from "../../icons/WebDevelopmentIcon.vue";
import TypographyVue from "@/components/main/TypographyVue.vue";
import SpaceVue from "@/components/main/SpaceVue.vue";
export default {
  props: {
    title: {
      type: String,
      required: true,
    },
    description: {
      type: String,
      required: true,
    },
    icon: {
      type: String,
      required: true,
    },
  },
  components: { WebDevelopmentIcon, TypographyVue, SpaceVue },
};
</script>
<template>
  <div class="service">
    <div class="icon">
      <WebDevelopmentIcon />
    </div>
    <SpaceVue />
    <div class="content">
      <TypographyVue component="h4" color="#2B2B2B">
        {{ title }}
      </TypographyVue>
      <SpaceVue />
      <TypographyVue component="p" color="#767676">
        {{ description }}
      </TypographyVue>
    </div>
  </div>
</template>

<style scoped>
.service {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  background-color: white;
  padding: 20px;
}
</style>
