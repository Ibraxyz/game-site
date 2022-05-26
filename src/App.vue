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
import Container from "./components/Container.vue";
import GradientBackground from "./components/GradientBackground.vue";
import Card from "./components/Card.vue";

//logos
import logo1 from "./assets/images/steam 1.png";
import logo2 from "./assets/images/microsoft 1.png";
import logo3 from "./assets/images/xbox-3.png";
import logo4 from "./assets/images/Frame 50.png";
import logo5 from "./assets/images/play-28.png";

export default {
  components: {
    FullScreenImageSlider,
    TwoLineText,
    Typography,
    Button,
    Navbar,
    Container,
    GradientBackground,
    Card
  },
  data() {
    return {
      images: [bg1, batman, bg2, bg3, bg4],
      downArrowIcon: DownArrow,
      logos: [logo1, logo2, logo3, logo4, logo5]
    };
  },
};
</script>

<template>
  <!-- wrapper -->
  <div>

    <!-- header -->
    <FullScreenImageSlider :images="images">
      <Container>
        <div class="space-betwwen-content">
          <Navbar />
          <div class="centered-content">
            <TwoLineText text="GAMEWORLD DISTRIBUTORS" />
            <Typography text="Connecting Players & Games in an Immersive environment." variant="h1" />
            <br />
            <Button text="Join Now !" variant="filled"></Button>
          </div>
          <div style="padding: 20px;position:relative;top:-80px">
            <Button text="Scroll down">
              <img :src="downArrowIcon" alt="" class="shake-vertical" style="position: relative" />
            </Button>
          </div>
        </div>
      </Container>
    </FullScreenImageSlider>

    <!-- section 2 -->
    <GradientBackground>
      <div class="align-center">
        <div style="margin-bottom:171px">
          <img v-for="logo in logos" :src="logo" alt="" style="margin:32px 27px 20px 32px" />
        </div>
        <div style="max-width:532px;margin:auto;padding-bottom:80px">
          <TwoLineText accent="true" text="What we do" />
          <Typography text="Meeting the needs of players across the world" variant="h2" />
        </div>
        <div class="card-wrapper" style="padding-bottom:200px">
          <Card :img="images[0]" variant="green-top" mainTitle="Title one goes here.." />
          <Card :img="images[1]" variant="blue-top" mainTitle="Title two goes here.." />
          <Card :img="images[2]" variant="red-top" mainTitle="Title three goes here.." />
        </div>
      </div>
    </GradientBackground>

  </div>
</template>

<style scoped>
.align-center {
  text-align: center;
}

.card-wrapper {
  display: flex;
  justify-content: center;
  align-items: center;
}
</style>
