<template>
    <span class="present">{{present}}</span>
</template>

<script>
export default {
    name: 'present',
    props: ['present'],
}
</script>

<style scoped>
    span {
        cursor: pointer;
    }
</style>
