<script>
import Typography from "./Typography.vue";
export default {
    props: ['img', 'variant', 'mainTitle'],
    components: {
        Typography
    }
}
</script>

<template>
    <div class="wrapper" :class="variant">
        <div style="padding:24px">
            <div class="img-wrapper">
                <img :src="img" alt="" class="img" />
                <img src="../assets/images/Frame 88.png" class="img-icon" />
            </div>
        </div>
        <div class="main-title">
            <img src="../assets/images/Group 2095.png" alt="" />
            <div class="main-title-text">
                <Typography variant="bold-p" :text="mainTitle" align="align-left"/>
            </div>
        </div>
        <div style="padding:24px;box-sizing:border-box;">
            <Typography
                text="List of carefully selected, verified, high quality suppliers in different regions worldwide."
                variant="p" align="align-left"/>
        </div>
    </div>
</template>

<style scoped>
.wrapper {
    width: 20%;
    background: #20202E;
    box-sizing: border-box;
    margin: 10px;
}

.green-top {
    box-shadow: inset 0px 2px 0px #61FFDA;
}

.blue-top {
    box-shadow: inset 0px 2px 0px #7B61FF;
}

.red-top {
    box-shadow: inset 0px 2px 0px #FF626B;
}

.img {
    width: 100%;
    height: auto;
}

.img-wrapper {
    position: relative;
}

.img-icon {
    position: absolute;
    bottom: 3.5px;
    left: 0px;
}

.main-title {
    text-align: left;
    position: relative;
}

.main-title-text {
    z-index: 8;
    width: 100%;
    height: 100%;
    position: absolute;
    top: 0px;
    left: 0px;
    display: flex;
    box-sizing: border-box;
    padding-left: 24px;
}
</style>