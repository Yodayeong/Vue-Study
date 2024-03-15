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
    //data 영역
    //food1과 food2라는 두 가지 음식 데이터 정의
    data() {
        return {
            food1: "pizza",
            food2: "spaghetti",
        }
    },
    //watch 영역

    //1. food1의 경우, handler 속성을 통해 데이터 변경 시 실행되는 콜백 함수 정의
    //- deep: 객체나 배열의 내부 값까지 깊게 관찰
    //- immediate: 컴포넌트가 처음 마운트될 때 즉시 handler를 실행

    //2. food2의 경우 단순히 변경된 값을 출력하는 함수를 짧은 문법으로 정의
    watch: {
        food1: {
            handler: function (newVal, oldVal) {
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