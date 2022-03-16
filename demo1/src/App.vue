<template>
  <div id="app">
    <router-view />
  </div>
</template>

<script>
import index from "./router";
export default {
  name: "App",
  data() {
    return {
      msg: "Welcome to Your Vue.js App",
      router: [],
      activeName: "HelloWorld"
    };
  },
  mounted() {
    this.router = index.options.routes.filter(x => x.name);
  }
};
</script>

<style>
#app {
}
</style>
