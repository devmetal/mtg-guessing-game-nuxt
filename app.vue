<template>
  <NuxtLoadingIndicator />
  <nav class="flex shadow-md gap-2 p-2">
    <NuxtLink to="/game"> Game </NuxtLink>
    <NuxtLink to="/login"> Login </NuxtLink>
    <NuxtLink to="/register"> Register </NuxtLink>
  </nav>
  <NuxtLayout>
    <NuxtPage />
  </NuxtLayout>
</template>
