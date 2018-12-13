<template>
 <div class="reindeer animated bounce">
   <img src="../assets/reindeer.png">
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

  .reindeer {
    margin-top: 15px;
  }
</style>
