<template>
  <div>PassedBlock: {{ greeting }}</div>
</template>

<script setup>
defineProps({
  greeting: {
    type: String,
    required: true
  }
})
</script>
