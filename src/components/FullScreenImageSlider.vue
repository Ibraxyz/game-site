<script>
import SliderItem from './SliderItem.vue'
export default {
  components: {
    SliderItem
  },
  data() {
    return {
      activeSlideIndex: 0
    }
  },
  props: ['images']
}
</script>

<template>
  <div class="fsis-wrapper">
    <div class="fsis-images">
      <SliderItem v-for="(image, index) in images" :url="image"
        :isDisplayed="index === this.activeSlideIndex ? true : false" />
    </div>
    <div class="fsis-overlay"></div>
    <div class="fsis-content"></div>
  </div>
</template>

<style scoped>
.fsis-wrapper {
  position: relative;
  height: 100vh;
  background-color: #000000;
  z-index: 1;
}

.fsis-images {
  position: absolute;
  top: 0px;
  left: 0px;
  width: 100%;
  height: 100%;
  z-index: 2;
  overflow: hidden;
}

.fsis-overlay {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  z-index: 3;
  background: linear-gradient(360deg,
      rgba(28, 28, 40, 0.8) 0%,
      rgba(28, 28, 40, 0) 77.78%);
  transform: rotate(-180deg);
}

.fsis-content {
  position: absolute;
  top: 0px;
  left: 0px;
  width: 100%;
  height: 100%;
  z-index: 4;
}
</style>
