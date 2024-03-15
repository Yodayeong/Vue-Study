<!-- 
WatchVue.vue
두 개의 음식 데이터(food1, food2)를 관찰 
Vue.js 컴포넌트가 화면에 렌더링 될 때, 변경사항을 관찰하고 대응하는 동작을 수행
-->

<template>
  <div>
    <input type="text" v-model="food1" />
    <input type="text" v-model="food2" />
  </div>
</template>

<script>
export default {
    data() {
        return {
            food1: "pizza",
            food2: "spaghetti",
        }
    },
    watch: {
        food1: {
            handler: function(newVal, oldVal) {
                console.log(newVal, oldVal)
            },
            deep: true,
            immediate: true,
        },
        food2(val) {
            console.log('food2', val)
        },
    },
}
</script>

<style>

</style>