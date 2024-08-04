<script setup lang="ts">
const props = defineProps(["variant"]);
</script>

<template>
  <button class="rounded-full">
    <slot />
  </button>
</template>

<style>
button {
  @apply duration-300 transition-all;
}

button.md {
  @apply py-4 px-6 font-medium text-xl;
}
button.md-r-xl {
  @apply py-4 pl-6 pr-10 font-medium text-xl;
}
button.lg {
  @apply py-6 px-8 font-medium text-xl;
}
button.outline-button {
  @apply border border-black;
}
button.hover-black-button {
  @apply hover:bg-black hover:text-gray-100;
}
button.orange-button {
  @apply bg-orange-400 text-gray-100 font-medium;
}
</style>
