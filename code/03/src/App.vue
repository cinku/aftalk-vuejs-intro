<template>
  <div id="app" class="container">
    <img src="./assets/logo.png">
    <app-header :presents="presents" :max-presents="maxPresents" />
    <app-new-present v-if="presents.length < 10" v-on:addNewPresent="addPresent" />
    <app-list v-bind:presents="presents" @deletePresent="deletePresent" />
  </div>
</template>

<script>
import List from './components/List.vue';
import NewPresent from './components/NewPresent.vue';
import Header from './components/Header.vue';

export default {
  name: 'app',
  components: {
    appList: List,
    appNewPresent: NewPresent,
    appHeader: Header
  },
  data() {
    return {
      presents: [
        'test present',
      ],
      maxPresents: 10
    };
  },
  methods: {
    addPresent(present) {
      this.presents.push(present);
    },
    deletePresent(index) {
      this.presents.splice(index, 1);
    }
  }
}
</script>

<style lang="scss">
@import '../node_modules/bootstrap/scss/bootstrap.scss';
@import '../styles.scss';

#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
