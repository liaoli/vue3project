
<script setup>
import { onMounted } from 'vue'
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
</script>

<template>
  <div>生命周期函数</div>
</template>

