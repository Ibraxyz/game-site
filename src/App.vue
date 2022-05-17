<script>
import Button from './components/Button.vue';
import Navbar from './components/Navbar.vue';
import Typography from './components/Typography.vue';

export default {
  components: {
    Button,
    Navbar,
    Typography
  },
};
</script>

<template>
  <div>
    <div>{{ count }}</div>
    <Navbar></Navbar>
    <Button></Button>
  </div>
</template>

<style>
</style>
