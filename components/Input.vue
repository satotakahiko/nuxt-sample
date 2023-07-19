<script setup>
  import { inject } from 'vue'
  const { modelValue } = defineProps({
    modelValue: String
  })

  defineEmits(['update:modelValue'])

  const num = inject('num')
</script>

<template>
  <p>Hi! {{ modelValue }}</p>
  <p>{{ num }}</p>
  <input
    :value="modelValue"
    @input="$emit('update:modelValue', $event.target.value)"
  />
</template>