
<script setup>
import { onMounted, ref } from 'vue'
import sonCom from '@/components/son-com.vue'
// 导入生命周期函数
// 执行生命周期函数，传入回调
onMounted(() => {
  console.log('onMounted---1')
})
onMounted(() => {
  console.log('onMounted---2')
})
onMounted(() => {
  console.log('onMounted---3')
})

// 生命周期函数执行多次的时候，会按照顺序依次执行

const money = ref(1000)

const getMoney = () => {
   money.value += 100
}
const changeFn = (num) => {
  money.value -= num
}

</script>

<template>
  <div>
    <h1>父组件</h1>
    <button @click="getMoney">获取钱</button>
    <son-com @changeMoney="changeFn" car="奔驰" :money="money"></son-com>
  </div>
</template>
