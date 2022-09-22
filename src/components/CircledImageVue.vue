<template>
  <div class="image-container">
    <img class="circled-image" src="../assets/profile.jpg" />
  </div>
</template>

<style scoped>
.circled-image {
  border-radius: 50%;
  position: relative;
  display: block;
  width: 150px;
  height: 150px;
}
.image-container {
  height: fit-content;
  width: fit-content;
}

.image-container::after {
  content: "";
  bottom: 10%;
  right: 10%;
  background: #7eb942;
  box-shadow: 0px 4px 10px rgba(0, 0, 0, 0.15);
  display: block;
  padding: 8px;
  z-index: 2;
  border-radius: 50%;
  position: absolute;
}
</style>
