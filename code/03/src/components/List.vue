<template>
    <div class="row list-container">
        <app-present v-for="(present, index) in presents" v-bind:key="present" v-bind:present="present" @click.native="deletePresent(index)"></app-present>
        <p v-if="presents.length === 0">Add some presents ;)</p>
    </div>
</template>

<script>
import Present from './Present.vue';

export default {
    name: 'presentsList',
    props: {
        'presents': {
            required: true
        }
    },
    components: {
        appPresent: Present
    },
    methods: {
        deletePresent(index) {
            this.$emit('deletePresent', index);
        }
    }
}
</script>

<style>

</style>
