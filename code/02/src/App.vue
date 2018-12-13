<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <app-new-reindeer v-if="reindeers.length <= maxReindeers - 1" @addReindeer="addReindeer"></app-new-reindeer>
    <app-sled :reindeers="reindeers" :max-reindeers="maxReindeers"></app-sled>
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
      maxReindeers: 8,
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
@import './assets/styles.scss';

#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #fff;
  margin-top: 60px;
}
</style>
