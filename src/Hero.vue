<script setup>
import BookACall from "./BookACall.vue";
import { ref, onMounted, onUnmounted } from "vue";

const isMobile = ref(false);

const checkScreenSize = () => {
  isMobile.value = window.innerWidth < 1024; // 1024px matches lg breakpoint
};

onMounted(() => {
  checkScreenSize();
  window.addEventListener("resize", checkScreenSize);
});

onUnmounted(() => {
  window.removeEventListener("resize", checkScreenSize);
});
</script>

<template>
  <template v-if="!isMobile">
    <div class="width-content flex items-center">
      <!-- Desktop layout -->
      <div class="w-5/12 space-y-5 md:space-y-10">
        <h1
          class="font-Eczar text-xl font-bold leading-tight text-gray-700 sm:text-3xl md:text-3xl lg:text-4xl xl:text-6xl 2xl:text-7xl 3xl:text-7xl"
        >
          Launch your MVP in just 4 weeks
        </h1>
        <h2
          class="hello-button md:text-md w-fit rounded-lg py-1 px-2 font-work_sans text-sm font-semibold text-gray-700 md:py-3 md:px-5 lg:text-xl 2xl:text-xl 3xl:text-3xl"
        >
          Bring your ideas to life with a rapid MVP, built within a clear,
          upfront budget.
        </h2>
        <div class="gap-1 md:flex md:gap-10">
          <BookACall />
        </div>
      </div>

      <div class="flex w-7/12 justify-end">
        <img
          class="sm:h-[350px] md:h-[450px] lg:h-[550px] xl:h-[550px] 2xl:h-[650px] 3xl:h-[800px]"
          src="../public/assets/hero.svg"
          alt="user image"
        />
      </div>
    </div>
  </template>

  <template v-else>
    <div class="mb-12 flex w-full flex-col items-center">
      <!-- Mobile layout -->
      <img class="w-full" src="../public/assets/hero.svg" alt="user image" />
      <div class="mx-8 flex flex-col items-center space-y-5 md:space-y-10">
        <h1
          class="text-center font-Eczar text-4xl font-bold leading-tight text-gray-700"
        >
          Launch your MVP in just 4 weeks
        </h1>
        <h3
          class="hello-button md:text-md w-fit rounded-lg py-1 px-2 text-center font-work_sans text-sm font-semibold text-gray-700"
        >
          Bring your ideas to life with a rapid MVP, built within a clear,
          upfront budget.
        </h3>
        <div class="gap-1 md:flex md:gap-10">
          <BookACall />
        </div>
      </div>
    </div>
  </template>
</template>

<style scoped></style>
