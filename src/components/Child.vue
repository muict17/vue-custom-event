<template>
  <div>
    <input v-model="incrementValue" />
    <button @click="onIncrease">Click to Increase</button>
  </div>
</template>
<script>
export default {
  data() {
    return {
      incrementValue: 0
    };
  },
  methods: {
    onIncrease: function() {
      /* eslint-disable */

      console.log("from child: value = ", this.incrementValue);
      this.$emit("toParent", this.incrementValue);
    }
  }
};
</script>
