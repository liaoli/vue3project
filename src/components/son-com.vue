<script setup>
const props = defineProps({
  car: String,
  money: Number,
});

const emit = defineEmits(["changeMoney"]);

console.log(props.car);
console.log(props.money);

const buy = () => {
  emit("changeMoney", 1000);
};
</script>

<template>
  <div class="son">
    我是子组件
    <h1>{{ car }}</h1>
    <h1>{{ money }}</h1>
    <button @click="buy">购买{{ car }}</button>
  </div>
</template>

<style scoped>
.son {
  border: 1px solid #000;
  padding: 30px;
}
</style>