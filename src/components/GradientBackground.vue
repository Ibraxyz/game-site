<script></script>

<template>
    <div class="wrapper">
        <div class="grad_bg">
            <div class="ball1"></div>
            <div class="ball2"></div>
        </div>
        <div class="content">
            <slot></slot>
        </div>
    </div>
</template>

<style scoped>
.wrapper {
    position: relative;
}

.grad_bg {
    position: absolute;
    top: 0px;
    left: 0px;
    width: 100%;
    height: 100%;
    box-sizing: border-box;
    background-color: red;
    z-index: 6;
    display: flex;
    justify-content: space-between;
}

.ball1 {
    width: 516px;
    height: 516px;

    /* Medley/Gradient */

    background: linear-gradient(267.28deg, #7B61FF 24%, #AA82FF 73.95%);
    opacity: 0.2;
    filter: blur(200px);
}

.ball2 {
    /* Ellipse 509 */

    width: 389px;
    height: 389px;

    /* Medley/Gradient */

    background: linear-gradient(267.28deg, #7B61FF 24%, #AA82FF 73.95%);
    opacity: 0.2;
    filter: blur(200px);
}

.content {
    position: absolute;
    z-index: 7;
    top: 0px;
    left: 0px;
    width: 100%;
    height: 100%;
}
</style>