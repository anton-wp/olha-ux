<template>
  <button class="group relative">
    <div class="service-card">
      <div
        class="relative flex h-60 flex-col rounded-t-[38px] border-2 border-gray-400"
      >
        <div
          class="absolute left-0 top-0 h-full w-full rounded-t-[38px] blur-sm backdrop-blur-sm group-hover:bg-orange-400"
        />
        <div
          class="z-10 mb-32 border-b-2 border-gray-400 px-9 py-6 text-start text-2xl font-medium"
        >
          UI/ UX Design
        </div>
      </div>
      <div
        class="absolute left-0 right-0 top-44 z-10 mx-auto h-20 w-[80%] rounded-3xl bg-gray-700 opacity-70 duration-500 group-hover:top-40"
      />
      <div
        class="absolute left-0 right-0 top-48 z-20 mx-auto h-20 w-[90%] rounded-3xl bg-gray-500 duration-500 group-hover:top-44"
      />

      <NuxtImg
        class="relative z-30 -mt-9 w-full object-cover duration-500 group-hover:scale-110"
        src="/example1.png"
        alt="example1"
      />
    </div>
    <div
      class="absolute bottom-0 right-0 flex h-28 w-28 items-center justify-center rounded-full bg-gray-900 group-hover:bg-orange-400"
    >
      <IconsArrowRightTop class="h-16 w-16" />
    </div>
  </button>
</template>

<style>
.service-card {
  margin-left: -1px;
  position: relative;
  width: 416px;
  height: 508px;
  /* background-color: #ff7f50;  */

  clip-path: path(
    "M37 1H379C398.882 1 415 17.1177 415 37V338.5C415 358.382 398.882 374.5 379 374.5H356.049C316.976 374.5 285.468 406.488 286.057 445.556L286.433 470.457C286.736 490.549 270.532 507 250.437 507H37C17.1177 507 1 490.882 1 471V37C1 17.1178 17.1177 1 37 1Z"
  );
  border-radius: 20px; /* Радиус скругления углов */
}
</style>
