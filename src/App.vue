<template>
  <div id="app">
    <h1>Web Development Resources</h1>
    <!-- <Buttons></Buttons> -->
    <Resources></Resources>
  </div>
</template>

<script>
import Resources from "./components/resources";
// import Buttons from "./components/buttons";

export default {
  name: "App",
  components: {
    Resources
    // Buttons
  }
};
</script>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
}

h1 {
  text-align: center;
}
</style>
