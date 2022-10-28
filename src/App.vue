<template>
  <add-text></add-text>
</template>

<script>
import AddText from "./components/AddText.vue";

export default {
  name: "App",
  components: {
    AddText,
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
