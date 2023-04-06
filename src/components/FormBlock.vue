<template>
  <div>
    FormBlock: {{ greeting }}

    <passed-block v-bind="$attrs" />

    <form action="">
      input: <input class="border-2 focus:border-gray-900" type="text" v-model="greeting" />
      <custom-input v-model="greeting" />
    </form>
  </div>
</template>

<script setup>
import { ref, watch } from 'vue'
import PassedBlock from './PassedBlock.vue'
import CustomInput from './CustomInput.vue'

const props = defineProps({
  greeting: {
    type: String,
    required: true
  }
})
const emit = defineEmits(['update:greeting'])

const greeting = ref(props.greeting)

watch(greeting, () => emit('update:greeting', greeting.value))
</script>
