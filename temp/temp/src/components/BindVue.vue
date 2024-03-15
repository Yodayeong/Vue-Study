<template>
  <div>
    <ul>
        <li v-for="item in items" v-bind:key="item">{{ item }}</li>
    </ul>
    <ul>
        <li v-for="item in itemObjects" v-bind:key="item.name">{{ item.name }}</li>
    </ul>
  </div>
</template>

<script>
export default {
    data() {
        return {
            items: ["menu1", "menu2", "menu3"],
            itemObjects: [{name: '길동'}, {name: '명동'}],
        }
    }
}
</script>

<style>

</style>