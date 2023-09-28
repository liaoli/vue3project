<script setup>
import { inject } from 'vue';
const themeColor = inject('theme-color');
const count = inject('count');
const changeCount = inject('changeCount');
const clickFn = () => {
    changeCount(1000)
};
</script>

<template>
    <div>
        <h1>我是底层组件--{{ themeColor }}--{{ count }}</h1>
        <button @click="clickFn">点击改变count</button>
    </div>
</template>