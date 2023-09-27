
<script setup>
import { ref, watch } from 'vue'
const message = ref('vue3 watch')
const count = ref(0)
const name = ref('zhangsan')
// 1. 监视多个个数据的变化
watch([count, name], ([newCount, oldCount],[newName,oldName]) => {
  console.log(`count 发生了变化, ${newCount}, ${oldCount}`)
  console.log(`count 发生了变化, ${newName}, ${oldName}`)
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

