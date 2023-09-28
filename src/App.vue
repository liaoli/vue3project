<script setup>
import { ref,provide } from 'vue'
import CenterCom  from '@/components/center-com.vue'

// 夸层传递普通数据
provide('theme-color','pink')

const count = ref(99)
// 夸层传响应式数据
provide('count',count)

// 夸层传递函数
provide('changeCount',(num)=>{
  count.value = num
})


</script>

<template>
  <div>
    <h1>顶层组件</h1>
    <CenterCom></CenterCom>
  </div>
</template>