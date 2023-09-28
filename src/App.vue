<script setup>
import { ref } from 'vue'
import MyInput from './components/my-input.vue';
import MyInputCom from './components/my-input-com.vue';

const txt = ref('123456')


</script>

<template>
  <div>
    <h1>顶层组件</h1>
    <MyInput v-model="txt"></MyInput>
    <p>{{ txt }}</p>
    <MyInputCom v-model="txt"></MyInputCom>
  </div>
</template>