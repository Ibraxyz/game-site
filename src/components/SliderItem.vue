<script>
let anim = null;
export default {
  props: ["url", "isDisplayed", "isBeginToGrad"],
};
</script>

<template>
  <div
    class="slider-item"
    :class="[{ 'display-none': !isDisplayed }, { 'fade-out': isBeginToGrad }]"
    :style="{ backgroundImage: `url(${url})` }"
  ></div>
</template>

<style scoped>
.slider-item {
  width: 100%;
  height: 100%;
  background-attachment: fixed;
  background-size: cover;
  background-repeat: no-repeat;
}

.display-none {
  display: none;
}
</style>
