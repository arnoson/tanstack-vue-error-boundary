<template>
  <div>
    <NuxtErrorBoundary>
      <MyComponent />
      <template #error="{error}">{{ error }}</template>
    </NuxtErrorBoundary>
  </div>
</template>