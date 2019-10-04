<template>
  <div id="app">
    <h1>Web Development Resources</h1>
    <Resources></Resources>
  </div>
</template>

<script>
import Resources from "./components/resources";

export default {
  name: "App",
  components: {
    Resources
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
