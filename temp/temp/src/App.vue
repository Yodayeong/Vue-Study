<template>
  <div id="app">
    <start-vue></start-vue>
    <bind-vue></bind-vue>
  </div>
</template>

<script>
import StartVue from './components/StartVue.vue'
import BindVue from './components/BindVue.vue'

export default {
  name: 'App',
  components: {
    StartVue,
    BindVue,
  },
}
</script>

<style></style>
