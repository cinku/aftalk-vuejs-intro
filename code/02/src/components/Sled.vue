<template>
  <div class="sled-container" :style="{ 'flex-direction': reindeers.length === 0 ? 'column' : 'row' }">

    <div class="santa" :class="{ 'animated wobble infinite': reindeers.length === 0 }">
      <img src="../assets/santa.png">
    </div>
  </div>
</template>

<script>
export default {

};
</script>

<style lang="scss" scoped>
</style>
