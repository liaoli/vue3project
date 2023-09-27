<!-- <script>
export default {
  name: "App",
  setup () {
    console.log('setup')
    const message = 'Hello vue3'

    const logMessage = () => {
      console.log(message)
    }

    return {
      message,
      logMessage
    };
  },
}
</script> -->
<!-- setup 语法糖 -->
<script setup>
import { reactive } from 'vue';
const message = 'reactive vue3'

const state = reactive({
  count: 0
})
const setCount = () => {
  state.count++
}
</script>

<template>
  <div>{{ message }}</div>
  <button @click="setCount">点我{{ state.count }}</button>
</template>

<style scoped>
header {
  line-height: 1.5;
}

.logo {
  display: block;
  margin: 0 auto 2rem;
}

@media (min-width: 1024px) {
  header {
    display: flex;
    place-items: center;
    padding-right: calc(var(--section-gap) / 2);
  }

  .logo {
    margin: 0 2rem 0 0;
  }

  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  }
}
</style>
