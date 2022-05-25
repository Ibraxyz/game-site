<script>
import logo1 from "../assets/images/Vector.png";
import SearchBar from "./SearchBar.vue";

export default {
  components: {
    SearchBar
  },
  data() {
    return {
      logo: logo1
    }
  }
}
</script>

<template>
  <nav class="navbar">
    <ul>
      <li style="margin-right: auto;display:flex;justify-content:center;align-items:center"><img :src="logo" alt=""
          style="margin-right:8px" />GameSite</li>
      <li>Home</li>
      <li>About</li>
      <li>Privacy Policy</li>
      <li>Our Shop</li>
      <li>
        <SearchBar />
      </li>
    </ul>
  </nav>
</template>

<style>
.navbar {
  width: 100%;
  box-sizing: border-box;
  padding: 17.67px;
}

.navbar ul {
  display: flex;
  justify-content: flex-end;
  align-items: center;
  list-style: none;
}

.navbar ul li {
  margin: 0px 20px;
  cursor: pointer;
  color: #fff;
}
</style>
