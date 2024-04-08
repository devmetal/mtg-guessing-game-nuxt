<script lang="ts" setup>
const url = "https://api.scryfall.com/cards/random?q=-t:land%20year%3E2000";
const { data: card } = await useFetch<ScryCard>(url);
</script>

<template>
  <img :src="card?.image_uris?.png" class="w-80" />
</template>

<style scoped></style>
