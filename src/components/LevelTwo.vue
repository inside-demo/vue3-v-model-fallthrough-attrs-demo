<template>
  <level-container label="LevelTwo">
    {{ greeting }}
    <em>
      There is no <code class="text-green-500">greeting</code> because it used in parent component
    </em>
  </level-container>
</template>

<script setup>
import LevelContainer from './LevelContainer.vue'

defineProps({
  greeting: {
    type: String,
    required: true
  }
})
</script>
