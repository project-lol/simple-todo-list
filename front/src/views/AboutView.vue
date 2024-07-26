<script setup>
import { ref } from 'vue'
const text = ref('hello world')
const titleClass = ref('title')
const count = ref(0)
const awesome = ref(false)

const changeTitleColor = () => {
  titleClass.value = 'title-blue'
}

const incrementCount = () => {
  count.value++
}

const toggleAwesome = () => {
  awesome.value = !awesome.value
}
</script>

<template>
  <h1 :class="titleClass">{{ text }}</h1>
  <button @click="changeTitleColor">Change title color</button>
  <p>Count: {{ count }}</p>
  <button @click="incrementCount">Increment count</button>

  <br />
  <input v-model="text" />

  <p v-if="awesome">Awesome is true</p>
  <p v-else>Awesome is false</p>
  <button @click="toggleAwesome">Toggle awesome</button>

  <!-- // https://vuejs.org/tutorial/#step-7 -->
</template>

<style>
.title {
  color: red;
}

.title-blue {
  color: blue;
}
</style>
