<template>
<div class="row">
    <div class="input-group">
        <input type="text" class="form-control" v-model.trim="newPresent" @keyup.enter="addPresent" />
        <button class="btn btn-success" v-on:click="addPresent">Add present</button>
    </div>
    </div>
</template>

<script>
export default {
  data() {
    return {
      newPresent: ""
    };
  },
  methods: {
      addPresent() {
          this.$emit('addNewPresent', this.newPresent);
          this.newPresent = '';
      }
  }
};
</script>

<style>

</style>
