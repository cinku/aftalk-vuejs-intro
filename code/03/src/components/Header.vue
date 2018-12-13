<template>
    <div class="row text-center">
        <h2><strong>Presents Added</strong></h2>
        <div class="progress">
            <div class="progress-bar" :style="{ width: (presentsNumber * 10) + '%' }">
                {{presentsNumber}} / {{maxPresents}}
            </div>
        </div>
    </div>
</template>

<script>
export default {
  props: ["presents", "maxPresents"],
  computed: {
      presentsNumber() {
          return this.presents.length;
      }
  }
};
</script>

<style>

</style>
