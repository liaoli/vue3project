<script setup>
import { ref, watch } from 'vue'
const message = ref('vue3 watch')
const count = ref(0)
const name = ref('zhangsan')
// 1. immediate 在侦听器创建时立即出发回调，响应式数据变化之后继续执行回调
watch(count, (newValue, oldValue) => {
  console.log(`count 发生了变化, ${newValue}, ${oldValue}`)
}, { immediate: true })

watch(name, (newValue, oldValue) => {
  console.log(`name 发生了变化, ${newValue}, ${oldValue}`)
})

const changCount = () => {
  count.value++
}
const changName = () => {
  name.value = 'lisi'
}
</script>

<template>
  <div>{{ message }}</div>
  <button @click="changCount">{{ count }}</button>
  <button @click="changName">{{ count }}</button>
</template>

