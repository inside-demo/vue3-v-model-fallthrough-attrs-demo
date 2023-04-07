<template>
  <level-container label="LevelOne">
    <greeting-wrapper>
      {{ greeting }}
    </greeting-wrapper>

    <level-two v-bind="$attrs" />

    <form action="">
      <level-container label="input">
        <greeting-wrapper>
          <input class="border-2 focus:border-gray-900" type="text" v-model="greeting" />
        </greeting-wrapper>
      </level-container>

      <custom-input v-model="greeting" />
    </form>
  </level-container>
</template>

<script setup>
import { ref, watch } from 'vue'
import LevelContainer from './LevelContainer.vue'
import GreetingWrapper from './GreetingWrapper.vue'
import LevelTwo from './LevelTwo.vue'
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
