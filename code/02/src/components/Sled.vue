<template>
  <div class="sled-container" :style="{ 'flex-direction': reindeers.length === 0 ? 'column' : 'row' }">
    <div v-if="reindeers.length === 0">
      <h2>Add some reindeers to pull poor santa's sled :(</h2>
    </div>
    <div v-else class="reindeers">
      <app-reindeer v-for="(reindeer, index) of reindeers" :reindeer="reindeer" :key="index"></app-reindeer>
    </div>
    <div class="santa" :class="{ 'animated wobble infinite': reindeers.length === 0 }">
      <img src="../assets/santa.png">
    </div>
  </div>
</template>

<script>
import Reindeer from './Reindeer.vue';

export default {
  props: ['reindeers'],
  components: {
    appReindeer: Reindeer,
  },
};
</script>

<style lang="scss" scoped>
.reindeers {
  display: flex;
  flex-direction: column;
  flex-wrap: wrap-reverse;
  align-content: flex-start;
  padding: 10px 25px;
}

.sled-container {
  display: flex;
  width: 60%;
  margin: 0 auto;
  height: 440px;
  justify-content: flex-end;
}

.santa {
  margin-left: 60px;
  display: flex;
  align-self: center;
}

img {
  width: 220px;
  height: 220px;
}
</style>
