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
    keywords: {
      type: String,
      required: true,
    },
  },
  data: function () {
    return {
      show: false,
    };
  },
  components: { WebDevelopmentIcon, TypographyVue, SpaceVue },
};
</script>
<template>
  <div class="service" @mouseenter="show = true" @mouseleave="show = false">
    <div class="general" v-if="!show">
      <WebDevelopmentIcon />
      <SpaceVue />
      <TypographyVue component="h4" color="#2B2B2B">
        {{ title }}
      </TypographyVue>
      <SpaceVue />
      <TypographyVue component="p" color="#767676">
        {{ keywords }}
      </TypographyVue>
    </div>
    <div class="detailed" :class="{ hide: !show }">
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
  cursor: pointer;
}

.hide {
  display: none;
}
</style>
