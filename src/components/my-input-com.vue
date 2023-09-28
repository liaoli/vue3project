<script setup>
defineProps({
    modelValue: {
        type: String,
        default: ''
    }
})

const emit = defineEmits(['update:modelValue'])

</script>

<template>
    <h2>我是中间组件</h2>
    <div>
        <input type="text"
        :value="modelValue"
        @input="e => emit('update:modelValue', e.target.value)"
        >
    </div>
</template>