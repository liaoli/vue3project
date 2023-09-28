




<script setup>
import { onMounted, ref } from 'vue'
import TestCom  from '@/components/test-com.vue'
// 模板引用(可以获取dom，也可以获取组件)
// 1. 调用ref函数，生成一个ref对象
// 2. 通过ref标识，进行绑定
// 3. 通过ref对象.value即可访问到绑定的元素(必须渲染完成后，才能拿到)
onMounted(() => {
  console.log('onMounted---1')
})


// 生命周期函数执行多次的时候，会按照顺序依次执行

const inp = ref(null)

const clickFn = () => {
  inp.value.focus()
}

const getCom = () => {
  console.log(testRef.value.count)
  testRef.value.sayHello()
}

</script>

<template>
  <div>
    <input type="text" ref="inp">
    <button @click="clickFn">点击让输入框获取焦点</button>
  </div>
  <TestCom ref="testRef"></TestCom>
  <button @click="getCom">获取组件</button>
</template>