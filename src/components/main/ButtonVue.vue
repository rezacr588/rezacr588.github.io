<template>
  <button class="button"><slot></slot></button>
</template>

<style scoped>
.button {
  display: flex;
  justify-content: center;
  align-items: center;
  padding: 16px 32px;
  gap: 10px;
  height: 51px;
  background: #ffb400;
  border-radius: 5px;
  outline: none;
  border: none;
  width: fit-content;
  cursor: pointer;
}
</style>
