<script setup>
import { ref } from 'vue'
import FormBlock from './components/FormBlock.vue'

const greeting = ref('Hello!')
</script>

<template>
  <header class="text-center">
    <img alt="Vue logo" class="logo" src="./assets/logo.svg" width="32" height="32" />
  </header>

  <main>
    <div>App: {{ greeting }}</div>

    <form-block v-model:greeting="greeting" />
  </main>
</template>
