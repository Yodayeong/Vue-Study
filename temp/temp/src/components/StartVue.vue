<template>
  <div>
    <h1 v-if="show">Loading....</h1>
    <button v-on:click="checkFunc()">click</button>
  </div>
</template>

<script>
export default {
    data() {
        return {
            show: false,
        }
    },
    methods: {
        checkFunc() {
            this.show = !this.show;
        },
    },
}
</script>

<style>

</style>