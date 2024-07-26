<script setup>
import { ref } from 'vue'
const text = ref('hello world')
const titleClass = ref('title')
const count = ref(0)

const changeTitleColor = () => {
  titleClass.value = 'title-blue'
}

const incrementCount = () => {
  count.value++
}
</script>

<template>
  <h1 :class="titleClass">{{ text }}</h1>
  <button @click="changeTitleColor">Change title color</button>
  <p>Count: {{ count }}</p>
  <button @click="incrementCount">Increment count</button>

  <br />
  <input v-model="text" />
</template>

<style>
.title {
  color: red;
}

.title-blue {
  color: blue;
}
</style>
