<template>
  <TestWorld
    title="Welcome to Vue Circles, Have Fun!"
  />
</template>

<script>
import TestWorld from "./components/TestWorld.vue";

export default {
  name: "App",
  components: {
    TestWorld,
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
