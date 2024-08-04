<script setup>
import { menu } from "@/constants/menu.js";
</script>

<template>
  <div class="rounded-t-3xl bg-gray-950 px-16 pt-16 pb-6">
    <div class="max-w-7xl mx-auto">
      <div class="flex justify-between pb-20 border-b border-gray-400">
        <div class="text-5xl font-semibold text-gray-100">
          Lets Connect there
        </div>
        <FormButton class="group md-r-xl orange-button flex relative pr-8">
          Hire me
          <IconsArrowRightTop
            class="absolute right-1 top-2 w-9 group-hover:rotate-45"
          />
        </FormButton>
      </div>
      <div class="py-10 flex justify-between text-gray-100 gap-6">
        <div class="max-w-xs lg:max-w-md xl:max-w-xl">
          <div>Logo</div>

          <div>
            Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed congue
            interdum ligula a dignissim. Lorem ipsum dolor sit amet, consectetur
            adipiscing elit. Sed lobortis orci elementum egestas lobortis.
          </div>
        </div>
        <div>
          <div class="mb-6 text-orange-400 font-semibold">Navigation</div>
          <div class="flex flex-col gap-3 text-sm">
            <nuxt-link
              class="hover:underline"
              v-for="item in menu"
              :to="item.link"
            >
              {{ item.label }}
            </nuxt-link>
          </div>
        </div>
        <div>
          <div class="mb-6 text-orange-400 font-semibold">Contact</div>
          <div class="flex flex-col gap-3 text-sm">
            <span> +91 7738443636 </span>
            <span> Jaycrea36@gmail.com </span>
            <span> Portfolio-jcrea.com </span>
          </div>
        </div>
        <div class="w-80">
          <div class="mb-6 text-orange-400 font-semibold">
            Get the latest information
          </div>
          <div class="relative">
            <input
              class="w-full h-10 pr-11 rounded-xl bg-white px-3 text-sm text-gray-950"
              type="text"
              placeholder="Email Address"
              name=""
              value=""
            />
            <button
              class="flex justify-center items-center absolute h-full w-11 right-0 top-0 rounded-r-xl bg-orange-400"
            >
              <IconsPaperPlant />
            </button>
          </div>
        </div>
      </div>
      <div
        class="border-t border-gray-400 text-gray-200 pt-10 flex justify-between"
      >
        <div>Copyright© 2023 Jayesh. All Rights Reserved.</div>
        <div class="">
          <nuxt-link class="hover:underline" to="/"
            >User Terms & Conditions</nuxt-link
          >
          |
          <nuxt-link class="hover:underline" to="/">Privacy Policy</nuxt-link>
        </div>
      </div>
    </div>
  </div>
</template>
