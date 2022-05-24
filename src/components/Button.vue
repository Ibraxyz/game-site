<script>
export default {
  props: {
    text: {
      type: String,
      required: true,
    },
    variant: {
      type: String,
      required: true,
    },
  },
};
</script>

<template>
  <button :class="variant === 'filled' ? 'purple_bg' : 'transparent_bg'">
    <span style="margin-right: 10px;">{{ text }}</span>
    <slot></slot>
  </button>
</template>

<style>
.purple_bg {
  background: linear-gradient(267.28deg, #7b61ff 24%, #aa82ff 73.95%);
  backdrop-filter: blur(4px);
  /* Note: backdrop-filter has minimal browser support */
  border-radius: 100px;
  color: #ffffff;
  padding: 18.5px 40px;
  box-shadow: none;
  border: 0;
  cursor: pointer;
  font-family: "Gotham";
  font-style: normal;
  font-weight: 700;
  font-size: 16px;
  line-height: 19px;

  /* Medley/Neutral */

  color: #ffffff;
}

.transparent_bg {
  background-color: rgba(255, 0, 0, 0.0);
  padding: 18.5px 40px;
  color: #ffffff;
  box-shadow: none;
  border: 0;
  cursor: pointer;
  font-family: "Gotham";
  font-style: normal;
  font-weight: 700;
  font-size: 16px;
  line-height: 19px;
}
</style>
