<script>
export default {
    props: ['url', 'isDisplayed']
};
</script>

<template>
    <div class="slider-item" :class="[{ 'fade-out': !isDisplayed },{ 'fade-in': isDisplayed }]" :style="{ backgroundImage: `url(${url})` }"></div>
</template>

<style scoped>
.slider-item {
    width: 100%;
    height: 100%;
    background-attachment: fixed;
    background-size: cover;
    background-repeat: no-repeat;
}
</style>
