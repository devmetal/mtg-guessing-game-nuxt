<script lang="ts" setup>
const props = defineProps<{
  card: ScryCard;
}>();
</script>

<template>
  <div class="w-80 flex flex-col justify-center gap-2">
    <img :src="$props.card?.image_uris?.png" class="w-full" />
    <p class="text-sm text-center pt-2 font-bold">
      Guess the color by picking the right ones
    </p>
    <div class="flex gap-1 justify-center">
      <Symbol image="black" />
      <Symbol image="green" />
      <Symbol image="blue" />
      <Symbol image="red" />
      <Symbol image="white" />
      <Symbol image="colorless" />
    </div>
    <div class="flex p-2">
      <input
        type="number"
        placeholder="Converted Mana Cost"
        class="border-2 outline-none border-black rounded-md w-full p-2"
      />
    </div>
    <div class="flex p-2 justify-center">
      <button
        class="outline-none p-2 shadow-md bg-amber-300 rounded-md px-4 font-bold"
      >
        Make a guess
      </button>
    </div>
  </div>
</template>

<style scoped></style>
