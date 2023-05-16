<template>
  <div>
    <button @click="throwNormalError">Throw normal error</button>
    <button @click="throwMutationError">Throw mutation error</button>
  </div>
</template>

<script setup lang="ts">
import { useMutation } from '@tanstack/vue-query';

const throwNormalError = () => {
  throw createError('normal error')
}

const mutation = useMutation(() => {
  throw createError('mutation error')
}, { useErrorBoundary: true })

const throwMutationError = () => mutation.mutate()
</script>