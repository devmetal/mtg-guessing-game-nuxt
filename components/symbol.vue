<script lang="ts" setup>
const props = defineProps<{
  image: "black" | "blue" | "colorless" | "green" | "red" | "white";
}>();

const icon = (await import(`./symbols/${props.image}.webp`)).default;
</script>

<template>
  <img :src="icon" :alt="$props.image" class="w-12" />
</template>
