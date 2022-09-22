// icon button with pop up
<script setup>
import IconVue from "./IconVue.vue";
</script>
<template>
  <div
    @mouseover="showPopUp = true"
    @mouseleave="showPopUp = false"
    class="icon-button"
  >
    <IconVue :active="showPopUp" size="40px" :name="icon" />
    <div class="pop-up" v-if="showPopUp">
      <slot name="pop-up"></slot>
    </div>
  </div>
</template>

<script>
export default {
  name: "IconButton",
  props: {
    icon: {
      type: String,
      required: true,
    },
  },
  data() {
    return {
      showPopUp: false,
    };
  },
};
</script>

// Language: vue // Path: src/components/main/IconButton.vue
<style scoped>
.icon-button {
  position: relative;
  display: inline-block;
  cursor: pointer;
}
.pop-up {
  position: absolute;
  opacity: 0;
  background: #2b2b2b;
  border-radius: 4px;
  box-shadow: 0 0 5px rgba(0, 0, 0, 0.2);
  padding: 10px;
  left: -40%;
  height: 24px;
  width: 180%;
  color: white;
  bottom: 120%;
  display: flex;
  justify-content: center;
  align-items: center;
  z-index: 1;
}
.icon-button:hover .pop-up {
  opacity: 1;
}

.pop-up::after {
  content: "";
  position: absolute;
  top: 100%;
  left: 50%;
  margin-left: -5px;
  border-width: 5px;
  border-style: solid;
  border-color: #2b2b2b transparent transparent transparent;
}
</style>
