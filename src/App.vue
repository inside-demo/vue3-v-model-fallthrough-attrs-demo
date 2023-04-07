<template>
  <header class="flex p-2 pt-4">
    <a
      class="inline-flex hover:opacity-75"
      href="https://github.com/inside-demo/vue3-v-model-fallthrough-attrs-demo"
    >
      <img class="mr-2" alt="Vue logo" src="./assets/logo.svg" width="32" height="32" />
      <span>vue3-v-model-fallthrough-attrs-demo</span>
    </a>
  </header>

  <main>
    <level-container label="App">
      <greeting-wrapper>
        {{ greeting }}
      </greeting-wrapper>

      <level-one v-model:greeting="greeting" />
    </level-container>
  </main>
</template>

<script setup>
import { ref } from 'vue'
import LevelContainer from './components/LevelContainer.vue'
import LevelOne from './components/LevelOne.vue'
import GreetingWrapper from './components/GreetingWrapper.vue'

const greeting = ref('Hello!')
</script>
