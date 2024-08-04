<script setup>
import { menu } from "@/constants/menu.js";
</script>

<template>
  <div class="rounded-full z-50 bg-black flex p-2 gap-4 w-fit mx-auto">
    <LayoutsLink v-for="item in menu.slice(0, 3)" :to="item.link">
      {{ item.label }}
    </LayoutsLink>
    <div class="lg:w-36 xl:w-48 text-white">LOGO</div>
    <LayoutsLink v-for="item in menu.slice(3, 6)" :to="item.link">
      {{ item.label }}
    </LayoutsLink>
  </div>
</template>
