<template>
  <div id="app">
    <start-vue></start-vue>
    <input-vue></input-vue>
    <bind-vue></bind-vue>
    <watch-vue></watch-vue>
  </div>
</template>

<script>
import StartVue from './components/StartVue.vue'
import BindVue from './components/BindVue.vue'
import WatchVue from './components/WatchVue.vue'
import InputVue from './components/InputVue.vue'

export default {
  name: 'App',
  components: {
    StartVue,
    InputVue,
    BindVue,
    WatchVue,
  },
}
</script>

<style></style>
