<template>
  <div>
    <h2>With NuxtErrorBoundary</h2>
    <NuxtErrorBoundary>
      <MyComponent />
      <template #error="{error}">{{ error }}</template>
    </NuxtErrorBoundary>
    <hr />
    <h2>With Custom Error Boundary</h2>
    <MyErrorBoundary>
      <MyComponent />
    </MyErrorBoundary>
  </div>
</template>