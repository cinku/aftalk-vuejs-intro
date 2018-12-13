<template>
  <div class="input-group">
      <input v-model.trim="reindeer" @keyup.enter="addReindeer">
      <button class="button" @click="addReindeer" :class="{ 'button-disabled': !reindeer }">Add reindeer</button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      reindeer: '',
    };
  },
  methods: {
    addReindeer() {
      if (!this.reindeer) return;
      this.$emit('addReindeer', this.reindeer);
      this.reindeer = '';
    },
  },
};
</script>

<style lang="scss" scoped>

</style>

