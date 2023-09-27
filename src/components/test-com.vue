<script setup>
const count = 99
const sayHello = () => {
    console.log('hello')
}

defineExpose({
    count,
    sayHello
})
</script>

<template>
    <div>test-com-{{ count }}</div>
</template>