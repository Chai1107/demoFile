<template>
  <div class="hello">
    HelloWorld2
    <Button @click="btn">111</Button>
  </div>
</template>

<script>
export default {
  name: "HelloWorld2",
  props: {
    list: {
      type: Array,
      default: () => []
    }
  },
  data() {
    return {
      msg: "Welcome to Your Vue.js App",
      index: 2
    };
  },
  methods: {
    btn() {
      console.log(this.list[this.index]);
    }
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped></style>
