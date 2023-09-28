<script setup>
import { defineModel } from 'vue'
const modelValue = defineModel()
</script>

<template>
    <h2>我是中间组件</h2>
    <div>
        <input type="text"
        :value="modelValue"
        @input="modelValue = $event.target.value"
        >
    </div>
</template>