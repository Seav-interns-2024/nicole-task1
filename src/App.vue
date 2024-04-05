<template>
  <Navbar />
  <div>
    <router-link to="/"></router-link>
</div>
  <router-view/>
</template>

<script>
import Navbar from './components/Navbar.vue';

export default {
    components: {
      Navbar
    },
}
</script>

<style>
#app {
  font-family: Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #333;
  margin-top: 60px;
}
body {
  margin: 0;
  background: #eee;
}
</style>
