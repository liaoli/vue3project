
<script setup>
// 1. reactive: 接收一个对象类型的数据，返回一个响应式的对象
//    问题：如果是简单类型，怎么办呢？
// import { reactive } from 'vue'
// const state = reactive({
//   count: 100
// })
// const setCount = () => {
//   state.count++
// }

// 2. ref: 接收简单类型 或 复杂类型，返回一个响应式的对象
//    本质：是在原有传入数据的基础上，外层包了一层对象，包成了复杂类型
//    底层，包成复杂类型之后，再借助 reactive 实现的响应式
//    注意点：
//    1. 脚本中访问数据，需要通过 .value
//    2. 在template中，.value不需要加 (帮我们扒了一层)

// 推荐：以后声明数据，统一用 ref => 统一了编码规范
import { ref } from 'vue';
const message = 'ref vue3'

const count = ref(0)
const setCount = () => {
  count.value++
}
</script>

<template>
  <div>{{ message }}</div>
  <button @click="setCount">点我{{ count }}</button>
</template>

<style scoped>
header {
  line-height: 1.5;
}

.logo {
  display: block;
  margin: 0 auto 2rem;
}

@media (min-width: 1024px) {
  header {
    display: flex;
    place-items: center;
    padding-right: calc(var(--section-gap) / 2);
  }

  .logo {
    margin: 0 2rem 0 0;
  }

  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  }
}
</style>
