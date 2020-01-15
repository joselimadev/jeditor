<template>
  <div id="app">
    <editor />
  </div>
</template>

<script>
import Editor from "./components/Editor.vue";

export default {
  name: "App",
  components: {
    Editor
  }
};
</script>

<style>
body {
  background-color: #2c3e50;
}
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
</style>
