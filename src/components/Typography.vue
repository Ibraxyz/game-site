<script>
export default {
  props: ['text', 'variant', 'align'],
}
</script>

<template>
  <h1 v-if="variant === 'h1'" :class="[variant, align]">{{ text }}</h1>
  <h2 v-else-if="variant === 'h2'" :class="[variant, align]">{{ text }}</h2>
  <h2 v-else-if="variant === 'p' || variant === 'bold-p'" :class="[variant, align]">{{ text }}</h2>
</template>

<style scoped>
.h1 {
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

.h2 {
  font-family: 'Gotham';
  font-style: normal;
  font-weight: 700;
  font-size: 32px;
  line-height: 40px;
  /* or 125% */

  text-align: center;

  color: #FFFFFF;


  /* Inside auto layout */

  flex: none;
  order: 2;
  flex-grow: 0;
}

.p {
  font-family: 'Gotham';
  font-style: normal;
  font-weight: 400;
  font-size: 14px;
  line-height: 21px;
  /* or 150% */

  /* Medley/Primary/100 */
  color: #DEE1FF;
}

.bold-p {
  font-family: 'Gotham';
  font-style: normal;
  font-weight: 700;
  font-size: 14px;
  line-height: 17px;
  /* identical to box height */


  /* Medley/Primary/100 */

  color: #DEE1FF;
}

.align-left {
  text-align: left;
}
</style>
