<script>
export default {
  props: ['text']
}
</script>

<template>
  <h1 class="large">{{ text }}</h1>
</template>

<style>
.large {
  font-family: "Gotham";
  font-style: normal;
  font-weight: 700;
  font-size: 48px;
  line-height: 58px;
  letter-spacing: -0.02em;
  color: #ffffff;
  mix-blend-mode: normal;
  display: inline-block;
  max-width: 1028px;
  text-align: center;
}
</style>
