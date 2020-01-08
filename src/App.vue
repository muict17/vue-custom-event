<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png" />
    <Child v-on:toParent="callFromChild" />
    {{ displayNumber }}
  </div>
</template>

<script>
import Child from "@/components/Child";
export default {
  name: "app",
  components: {
    Child
  },
  data() {
    return {
      displayNumber: 0
    };
  },
  methods: {
    callFromChild: function(value) {
      /* eslint-disable */
      console.log("Value from child => ", value);
      this.displayNumber = value;
    }
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
