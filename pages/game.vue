<script lang="ts" setup>
const url = "https://api.scryfall.com/cards/random?q=-t:land%20year%3E2000";
const { data: card } = await useFetch<ScryCard>(url);
</script>

<template>
  <div class="flex justify-center m-2">
    <Card :card="card!" />
  </div>
</template>

<style scoped></style>
