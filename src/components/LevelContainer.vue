<template>
  <div class="border-2 border-green-300 m-2">
    <div class="p-2 bg-green-200">
      {{ label }}
    </div>
    <div class="p-2">
      <slot></slot>
    </div>
  </div>
</template>

<script setup>
defineProps({
  label: {
    type: String,
    required: true
  }
})
</script>
