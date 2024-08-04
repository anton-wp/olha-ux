<script setup>
const experinceArr = [
  {
    place: "Cognizant, Mumbai",
    date: "Sep 2016- July 2020",
    position: "Experince Designer",
    experince:
      "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Duis lacus nunc, posuere in justo vulputate, bibendum sodales ",
    color: "#FD853A",
  },
  {
    place: "Sugee Pvt limited, Mumbai",
    date: "Sep 2020- July 2023",
    position: "UI/UX Designer",
    experince:
      "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Duis lacus nunc, posuere in justo vulputate, bibendum sodales ",
    color: "#1D2939",
  },
  {
    place: "Cinetstox, Mumbai",
    date: "Sep 2023",
    position: "Lead UX Designer",
    experince:
      "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Duis lacus nunc, posuere in justo vulputate, bibendum sodales ",
    color: "#FD853A",
  },
];

const selecter = ["Portfolio", "Hire me"];

const settings = {
  itemsToShow: 1,
  snapAlign: "center",
  autoplay: "8000",
};
const breakpoints = {
  // 700px and up
  856: {
    itemsToShow: 1.5,
    snapAlign: "center",
  },
  1024: {
    itemsToShow: 2,
    snapAlign: "center",
  },

  1280: {
    itemsToShow: 2.2,
    snapAlign: "start",
  },
  1440: {
    itemsToShow: 3,
    snapAlign: "start",
  },
};
</script>

<template>
  <div class="flex flex-col">
    <div class="relative flex flex-col">
      <div class="relative mx-auto mt-14">
        <IconsSmLines class="absolute -right-5 -top-5" />
        <FormButton class="md outline-button"> Hello! </FormButton>
      </div>
      <h1 class="mt-2 text-center text-8xl font-semibold">
        I’m <span class="text-orange-400">Jenny</span>,
        <br />
        Product Designer
      </h1>
      <div class="relative mx-auto">
        <div
          class="absolute bottom-12 left-0 right-0 mx-auto flex w-fit gap-2 overflow-hidden rounded-full border-2 border-gray-400 p-2"
        >
          <div class="absolute left-0 top-0 h-full w-full backdrop-blur-sm" />
          <button
            v-for="item in selecter"
            class="group z-10 flex rounded-full px-4 py-3 text-2xl font-light text-gray-100 hover:bg-orange-400 hover:px-6 hover:font-medium"
          >
            {{ item }}
            <IconsArrowRightTop class="hidden h-8 w-8 group-hover:block" />
          </button>
        </div>
        <NuxtImg src="/i-home-page.png" alt="i-home-page" />
      </div>
    </div>
    <div
      class="relative mx-auto max-h-[900px] w-full max-w-screen-2xl overflow-hidden rounded-3xl px-16 py-28 text-gray-100"
    >
      <div
        class="absolute left-0 top-0 z-10 h-full w-full bg-black opacity-70"
      />

      <NuxtImg
        class="absolute left-0 top-0 h-full w-full object-cover"
        src="/bg-with-line.jpeg"
      />
      <div class="relative z-10 mb-24 flex justify-between">
        <h5 class="text-4xl font-medium">
          My <span class="text-orange-400">Services</span>
        </h5>
        <div class="max-w-[50%] font-medium">
          Lorem ipsum dolor sit amet, consectetur adipiscing elit. Duis lacus
          nunc, posuere in justo vulputate, bibendum sodales
        </div>
      </div>

      <Carousel class="z-20" v-bind="settings" :breakpoints="breakpoints">
        <Slide v-for="slide in 10" :key="slide">
          <HomeMyServicesBlock />
        </Slide>

        <template #addons>
          <Pagination />
        </template>
      </Carousel>
    </div>
    <div class="mx-auto w-full max-w-6xl px-6 py-20">
      <h3 class="mb-20 text-center text-6xl font-medium">
        My
        <span class="text-orange-400"> Work Experince</span>
      </h3>
      <div
        class="relative flex flex-col items-center justify-center gap-10 overflow-y-hidden"
      >
        <IconsVerticalDashLine class="absolute top-0" />
        <div class="grid grid-cols-7" v-for="item in experinceArr">
          <div class="col-span-3 flex flex-col">
            <div class="text-2xl font-semibold text-black">
              {{ item.place }}
            </div>
            <div class="text-gray-500">
              {{ item.date }}
            </div>
          </div>
          <IconsSircleWithDashBorder
            class="z-10 mx-auto h-8 w-8"
            :fill="item.color"
          />
          <div class="col-span-3 flex flex-col">
            <div class="text-2xl font-semibold text-black">
              {{ item.position }}
            </div>
            <div class="text-gray-500">
              {{ item.experince }}
            </div>
          </div>
        </div>
      </div>
    </div>
    <div
      class="relative mx-auto flex h-32 w-full max-w-screen-2xl items-center overflow-hidden rounded-3xl bg-orange-400"
    >
      <div class="-mt-12 -rotate-1 bg-white py-4">
        <div class="marquee-content whitespace-nowrap">
          Это пример бегущей строки. Это пример бегущей строки. Это пример
          бегущей строки. Это пример бегущей строки. Это пример бегущей строки.
          Это пример бегущей строки. Это пример бегущей строки. Это пример
          бегущей строки. Это пример бегущей строки. Это пример бегущей строки.
          Это пример бегущей строки. Это пример бегущей строки. Это пример
          бегущей строки. Это пример бегущей строки. Это пример бегущей строки.
          Это пример бегущей строки.
        </div>
      </div>
    </div>
    <div class="w-full rounded-3xl bg-gray-300 px-9 py-14">
      <div class="mx-auto grid max-w-screen-xl grid-cols-2">
        <NuxtImg src="/whyHiredMy.png" />
        <div class="flex max-w-2xl flex-col justify-center">
          <h4 class="mb-10 text-5xl font-medium">
            Why <span class="text-orange-400">Hire me?</span>
          </h4>
          <div class="mb-10 text-lg text-gray-500">
            Lorem ipsum dolor sit amet, consectetur adipiscing elit. Duis lacus
            nunc, posuere in justo vulputate, bibendum sodales
          </div>
          <div class="mb-10 flex">
            <div class="flex-1">
              <div class="text-xl font-medium text-gray-950">450+</div>
              <div class="text-gray-600">Project Completed</div>
            </div>
            <div class="flex-1">
              <div class="text-xl font-medium text-gray-950">450+</div>
              <div class="text-gray-600">Project Completed</div>
            </div>
          </div>
          <FormButton class="lg outline-button hover-black-button w-fit">
            Hire me
          </FormButton>
        </div>
      </div>
    </div>
  </div>
</template>

<style>
.marquee-content {
  animation: scroll 10s linear infinite;
}

@keyframes scroll {
  from {
    transform: translateX(0);
  }
  to {
    transform: translateX(calc(-50% - 20px));
  }
}
</style>
