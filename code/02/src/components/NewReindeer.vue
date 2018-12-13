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
  .input-group {
    display: flex;
    width: 300px;
    flex-direction: column;
    margin: 0 auto;
  }

  input {  
    padding: .375rem .75rem;
    font-size: 1rem;
    line-height: 1.5;
    color: #495057;
    background-color: #fff;
    background-clip: padding-box;
    border: 1px solid #ced4da;
    border-radius: 2px;
    transition: border-color .15s ease-in-out,box-shadow .15s ease-in-out;
  }

  .button {
    margin: 5px 0;
    padding: 0;
    background-color: #8f191c;
    border-width: 0;
    outline: none;
    border-radius: 2px;
    box-shadow: 0 1px 4px rgba(0, 0, 0, .6);
    color: #ecf0f1;
    padding: 12px 24px;
    transition: background-color .3s;

    &-disabled {
      cursor: not-allowed;
    }

    &:not(&-disabled):hover {
      cursor: pointer;
      background-color: darken(#8f191c, 10%);
    }
  }
</style>

