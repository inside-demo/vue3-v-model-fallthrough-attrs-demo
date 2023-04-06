<template>
  <div>
    CustomInput:
    <input
      class="border-2 focus:border-gray-900"
      :value="modelValue"
      @input="$emit('update:modelValue', $event.target.value)"
    />
  </div>
</template>

<script setup>
defineProps(['modelValue'])
defineEmits(['update:modelValue'])
</script>
