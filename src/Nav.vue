<script setup>
import { ref } from "vue";
import BookACall from "./BookACall.vue";

const showMenu = ref(false);
</script>

<template>
  <nav
    class="width-content px-4 md:flex md:items-center md:justify-between lg:px-0"
  >
    <div class="flex items-center justify-between">
      <div class="relative mr-4">
        <img class="h-12 lg:h-20" src="../public/assets/logo.svg" alt="logo" />
      </div>
      <div
        class="font-Eczar text-xl font-bold text-gray-900 lg:block lg:text-3xl"
      >
        IdeaUnlock
      </div>
      <!-- Mobile menu button -->
      <div @click="showMenu = !showMenu" class="flex md:hidden">
        <button
          type="button"
          class="text-gray-800 hover:text-gray-400 focus:text-gray-400 focus:outline-none"
        >
          <svg viewBox="0 0 24 24" class="h-6 w-6 fill-current">
            <path
              fill-rule="evenodd"
              d="M4 5h16a1 1 0 0 1 0 2H4a1 1 0 1 1 0-2zm0 6h16a1 1 0 0 1 0 2H4a1 1 0 0 1 0-2zm0 6h16a1 1 0 0 1 0 2H4a1 1 0 0 1 0-2z"
            ></path>
          </svg>
        </button>
      </div>
    </div>
    <!-- Mobile Menu open: "block", Menu closed: "hidden" -->
    <ul
      :class="showMenu ? 'flex' : 'hidden'"
      class="mt-8 flex-col items-end space-y-4 md:mt-0 md:flex md:flex-row md:items-center md:space-y-0 md:space-x-10"
    >
      <li class="menu-button"><a href="#">Home</a></li>
      <li class="menu-button"><a href="#work" v-smooth-scroll>Works</a></li>
      <!--      <li class="menu-button">-->
      <!--        <a href="#testimonial" v-smooth-scroll>Testimonials</a>-->
      <!--      </li>-->
      <li class="menu-button"><a href="#about" v-smooth-scroll>About</a></li>
      <!--      <li class="menu-button">-->
      <!--        <a href="https://cal.com/maciek-chmura-idea-unlock">Book a call</a>-->
      <!--      </li>-->
      <li class="menu-button">
        <BookACall />
      </li>
    </ul>
  </nav>
</template>

<style scoped></style>
