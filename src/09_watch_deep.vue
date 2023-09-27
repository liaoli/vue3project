
<script setup>
import { ref, watch } from 'vue'
const message = ref('vue3 watch deep')
const count = ref({count: 0})
// 1. immediate 在侦听器创建时立即出发回调，响应式数据变化之后继续执行回调
watch(count, (newValue, oldValue) => {
  console.log(`count 发生了变化, ${newValue}, ${oldValue}`)
}, { deep: true })


const changCount = () => {
  count.value.count++
}

</script>

<template>
  <div>{{ message }}</div>
  <button @click="changCount">{{ count }}</button>
</template>

