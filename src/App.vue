
<script setup>
import { ref, computed } from 'vue';
const message = 'computed vue3'

const list = ref([1,2,3,4,5,6])
const sum = computed(() => {
  return list.value.reduce((pre, cur) => {
    return pre + cur
  })
})

const largeThen4 = computed(() => {
  return list.value.filter(item => item > 4)
})
</script>

<template>
  <div>{{list}}-{{ message }}</div>
  <button >数组的和{{ sum }}</button>
  <div>大于4的数组是{{ largeThen4 }}</div>
</template>

