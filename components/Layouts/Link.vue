<script setup lang="ts">
const props = defineProps(["to"]);
</script>

<template>
  <nuxt-link
    class="header-link block text-xl transition-all duration-300 text-white lg:px-6 lg:py-3 xl:px-10 xl:py-5 rounded-full hover:bg-slate-700"
    :to="to"
  >
    <slot />
  </nuxt-link>
</template>

<style>
.header-link.router-link-active {
  @apply bg-orange-400 font-bold;
}
</style>
