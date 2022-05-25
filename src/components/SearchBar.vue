<script>
import SearchIcon from "../assets/images/Group 2000.png";
export default {
    data() {
        return {
            searchIcon: SearchIcon
        }
    }
}
</script>

<template>
    <div class="bg">
        <input type="text"
            style="border-radius:34px;outline-width: 0;width:80%;border:none;position:relative;left:-0px" />
        <img :src="searchIcon" alt="" />
    </div>
</template>

<style scoped>
.bg {
    width: 219px;
    height: 36px;

    background: #FEFDFE;
    /* Medley/Grey/100 */

    border: 1px solid #E4E5EC;
    border-radius: 34px;

    display: flex;
    justify-content: flex-end;

    box-sizing: border-box;
    padding: 3px;
}
</style>