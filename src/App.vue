<script>
import FullScreenImageSlider from "./components/FullScreenImageSlider.vue";
import './assets/base.css';

//images
import bg1 from "./assets/images/bg1.png";
import batman from "./assets/images/batman.png";

export default {
  components: {
    FullScreenImageSlider,
  },
  data() {
    return {
      images: [bg1, batman]
    }
  }
};
</script>

<template>
  <div>
    <FullScreenImageSlider :images="images" />
  </div>
</template>

<style scoped>
</style>
