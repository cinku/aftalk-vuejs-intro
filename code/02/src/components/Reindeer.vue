<template>
 <div class="reindeer animated bounce">
   <img v-if="reindeer === 'Przenifer'" src="../assets/przenifer.png">
   <img v-else src="../assets/reindeer.png">
   <div>{{reindeer}}</div>
 </div>
</template>

<script>
export default {
  props: ['reindeer'],
};
</script>

<style lang="scss" scoped>
  img {
    width: 170px;
    height: 170px;
  }
</style>
