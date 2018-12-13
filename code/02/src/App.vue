<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <app-new-reindeer @addReindeer="addReindeer"></app-new-reindeer>
    <app-sled :reindeers="reindeers"></app-sled>
  </div>
</template>

<script>
import Sled from "./components/Sled.vue";
import NewReindeer from "./components/NewReindeer.vue";

export default {
  name: "app",
  components: {
    appSled: Sled,
    appNewReindeer: NewReindeer
  },
  data() {
    return {
      reindeers: [],
    };
  },
  methods: {
    addReindeer(reindeer) {
      this.reindeers.push(reindeer);
    }
  }
};
</script>

<style lang="scss">
@import '../node_modules/animate.css/animate.min.css';

#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #fff;
  margin-top: 60px;
}

body {
  background: #d1913c; /* fallback for old browsers */
  background: -webkit-linear-gradient(
    to right,
    #ffd194,
    #d1913c
  ); /* Chrome 10-25, Safari 5.1-6 */
  background: linear-gradient(
    to right,
    #ffd194,
    #d1913c
  ); /* W3C, IE 10+/ Edge, Firefox 16+, Chrome 26+, Opera 12+, Safari 7+ */
}
</style>
