<template>
  <div class="main">
    <h3>This is Home component.</h3>
    <router-link to="/about">Static About</router-link>
    <div id="list"></div>
    <button @click="addLink">Add Link</button>
  </div>
</template>

<script>
import $ from "jquery";
export default {
  name: "Home",
  data() {
    return {
      elementArray: [],
    };
  },

  methods: {
    addLink() {
      this.elementArray = [];
      this.elementArray.push(
        '<router-link to="/about">Dynamic About</router-link>'
      );
      $("#list").html(this.elementArray.join(""));
    },
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
* {
  margin: 2rem;
}
</style>
