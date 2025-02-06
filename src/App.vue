<template>
  <div id="app">

    <h1>Gen Ai & AI Agents</h1>
	<h2>Upload your data to get Gen Ai predictions</h2>
    <img
      alt="Vue logo"
      style="width: 100px; height: 100px"
      src="data:image/png;base64,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"
    />
    <br />
    <br />
    <HelloWorld msg="Welcome to Your Vue.js App" />
  </div>
</template>

<script>
import HelloWorld from "./components/HelloWorld.vue";

export default {
  name: "App",
  components: {
    HelloWorld,
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
