**Vue 기초문법**

**1) 간단한 준비 작업**

```vue
<!-- App.vue -->

<template>
  <div id="app">
    <start-vue></start-vue>
  </div>
</template>

<script>
import StartVue from './components/StartVue.vue'

export default {
  name: 'App',
  components: {
    StartVue,
  },
}
</script>

<style></style>
```

<br>

**2) 텍스트 바인딩**

```vue
<!-- StartVue.vue -->

<template>
  <h1>{{ message }}</h1>
</template>

<script>
export default {
    data() {
        return {
            message: "let's start!!",
        }
    },
}
</script>

<style>

</style>
```

* Vue의 template 태그 안에서 컴포넌트의 데이터를 렌더링하기 위해선 {{ data명 }}을 사용

<br>

**3) 반복 렌더링**

```vue
<!-- BindVue.vue -->

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
```

<br>

**4) v-model 사용**

```vue
<!-- StartVue.vue -->

<template>
  <input type="text" v-model="title" />
</template>

<script>
export default {
    data() {
        return {
            title: "",
        }
    },
}
</script>

<style>

</style>
```

* StartVue 컴포넌트의 title이 v-model을 통해 동적으로 바인딩(live server로 확인 가능)

<br>

**5) v-if 사용**

```vue
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
```

