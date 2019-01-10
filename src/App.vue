<template>
  <div id="app">
    <DumbSound />
  </div>
</template>

<script>
import DumbSound from "./components/DumbSound.vue";

export default {
  name: "App",
  components: {
    DumbSound
  }
};
</script>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
