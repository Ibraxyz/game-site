<script>
export default {
  props: {
    accent: {
      type: Boolean,
      required: true
    },
    text: {
      type: String,
      required: true
    }
  }
}
</script>

<template>
  <div class="center-div">
    <div :class="accent ? 'accent' : ' white-line'" style="display: inline-block; margin-left: 4px; margin-right: 4px">
    </div>
    <span :style="{
      color: accent ? '#F68E5F' : '#ffffff',
      display: 'inline-block',
      'margin-left': '4px',
      'margin-right': '4px',
    }">
      {{ text }}
    </span>
    <div :class="accent ? 'accent' : ' white-line'" style="display: inline-block; margin-left: 4px; margin-right: 4px">
    </div>
  </div>
</template>

<style scoped>
.white-line {
  width: 40px;
  height: 2px;

  /* Medley/Neutral */

  background: #ffffff;
  border-radius: 100px;
}

.center-div {
  display: flex;
  justify-content: center;
  align-items: center;
}

.accent {
  width: 40px;
  height: 2px;
  background: #F68E5F;
  border-radius: 100px;
}
</style>
