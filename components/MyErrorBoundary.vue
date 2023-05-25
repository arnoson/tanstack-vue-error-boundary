<template>
  <div v-if="hasError">{{ error }}</div>
  <div v-else>
    <slot></slot>
  </div>
</template>

<script setup lang="ts">
const hasError = ref(false)
const error = ref<Error | undefined>()

onErrorCaptured((capturedError) => {
  hasError.value = true
  error.value = capturedError
})

</script>