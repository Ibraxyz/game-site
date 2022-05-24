<script>
import FullScreenImageSlider from "./components/FullScreenImageSlider.vue";
import "./assets/base.css";

//images
import bg1 from "./assets/images/bg1.png";
import bg2 from "./assets/images/bg2.png";
import bg3 from "./assets/images/bg3.png";
import bg4 from "./assets/images/bg4.png";
import batman from "./assets/images/batman.png";
import TwoLineText from "./components/TwoLineText.vue";
import Typography from "./components/Typography.vue";
import Button from "./components/Button.vue";
import Navbar from "./components/Navbar.vue";
import DownArrow from "./assets/images/arrow_downward_24px.svg";

export default {
  components: {
    FullScreenImageSlider,
    TwoLineText,
    Typography,
    Button,
    Navbar
  },
  data() {
    return {
      images: [bg1, batman, bg2, bg3, bg4],
      downArrowIcon: DownArrow
    };
  },
};
</script>

<template>
  <div>
    <FullScreenImageSlider :images="images">
      <div class="space-betwwen-content">
        <Navbar />
        <div class="centered-content">
          <TwoLineText />
          <Typography />
          <br />
          <Button text="Join Now !" variant="filled"></Button>
        </div>
        <div style="padding: 20px">
          <Button text="Scroll down">
            <img :src="downArrowIcon" alt="" class="shake-vertical" style="position:relative" />
          </Button>
        </div>
      </div>
    </FullScreenImageSlider>
  </div>
</template>

<style scoped>
</style>
