<script setup>
import { ref } from 'vue'
import MyInput from './components/my-input.vue';
const txt = ref('123456')


</script>

<template>
  <div>
    <h1>顶层组件</h1>
    <MyInput v-model="txt"></MyInput>
    <p>{{ txt }}</p>
  </div>
</template>