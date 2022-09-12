<script>
export default {
  props: {
    title: { type: String, required: true },
  },
};
</script>

<template>
  <button class="button">{{ title }} <slot></slot></button>
</template>

<style scoped>
.button {
  display: flex;
  justify-content: center;
  align-items: center;
  padding: 16px 32px;
  gap: 10px;
  width: 154px;
  height: 51px;
  background: #ffb400;
  border-radius: 5px;
  outline: none;
  border: none;
  cursor: pointer;
}
</style>
