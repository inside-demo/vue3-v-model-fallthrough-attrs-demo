<template>
  <level-container label="CustomInput">
    <greeting-wrapper>
      <input
        class="border-2 focus:border-gray-900"
        :value="modelValue"
        @input="$emit('update:modelValue', $event.target.value)"
      />
    </greeting-wrapper>
  </level-container>
</template>

<script setup>
import LevelContainer from './LevelContainer.vue'
import GreetingWrapper from './GreetingWrapper.vue'

defineProps(['modelValue'])
defineEmits(['update:modelValue'])
</script>
