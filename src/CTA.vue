<script setup>
import BookACall from "./BookACall.vue";
</script>

<template>
  <div class="banner-1 flex h-full items-center" id="call">
    <div class="flex w-full flex-col items-center gap-8 p-12">
      <h2
        class="mt-2 text-center font-Eczar text-4xl font-semibold tracking-tight text-gray-700 lg:mt-10 lg:text-5xl"
      >
        Let’s work together and build your MVP.
      </h2>
      <img class="h-fit w-full lg:w-1/3" src="../public/assets/highfive.svg" />
      <BookACall />
    </div>
  </div>
</template>

<style scoped></style>
