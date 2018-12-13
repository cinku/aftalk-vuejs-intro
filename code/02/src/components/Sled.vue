<template>
  <div class="sled-container" :style="{ 'flex-direction': reindeers.length === 0 ? 'column' : 'row' }" :class="{ 'riding': reindeers.length === maxReindeers }">
    <div v-if="reindeers.length === 0">
      <h2>Add some reindeers to pull Santa's sled :(</h2>
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
  props: ['reindeers', 'maxReindeers'],
  components: {
    appReindeer: Reindeer,
  },
};
</script>

<style lang="scss" scoped>
</style>
