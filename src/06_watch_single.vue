
<script setup>
import { ref, watch } from 'vue';
const message = ref('vue3 watch');
const count = ref(0);
// 1. 监视单个数据的变化
watch(count, (newValue, oldValue) => {
  console.log(`count 发生了变化, ${newValue}, ${oldValue}`);
});

const changCount = () => {
  count.value++;
};

</script>

<template>
  <div>{{ message }}</div>
  <button @click="changCount">{{ count }}</button>
</template>

