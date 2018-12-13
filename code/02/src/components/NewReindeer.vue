<template>
  <div>
    <input v-model="reindeer" @keyup.enter="addReindeer">
    <button @click="addReindeer">Add reindeer</button>
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
      this.$emit('addReindeer', this.reindeer);
      this.reindeer = '';
    },
  },
};
</script>

<style>

</style>
