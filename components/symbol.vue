<script lang="ts" setup>
const active = ref(false);

const props = defineProps<{
  image: "black" | "blue" | "colorless" | "green" | "red" | "white";
}>();

const icon = (await import(`./symbols/${props.image}.webp`)).default;
</script>

<template>
  <img
    :src="icon"
    :alt="$props.image"
    class="w-12 cursor-pointer transition-transform"
    :class="{ '-translate-y-2': active }"
    @click="active = !active"
  />
</template>
