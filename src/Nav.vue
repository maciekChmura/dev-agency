<script setup></script>

<template>
  <nav
    class="container mx-auto px-6 md:flex md:items-center md:justify-between"
  >
    <div class="flex items-center justify-between">
      <div class="relative mr-4">
        <!--          <img-->
        <!--            class="rounded-full border border-gray-100 shadow-sm"-->
        <!--            src="https://images.unsplash.com/photo-1531746020798-e6953c6e8e04?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=512&h=512&q=80"-->
        <!--            alt="user image"-->
        <!--          />-->
        <img class="h-20" src="./assets/logo.svg" alt="logo" />
      </div>
      <div class="hidden font-Eczar text-3xl font-bold text-gray-900 lg:block">
        ideaUnlock
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
      <li class="menu-button">
        <a href="https://cal.com/maciek-chmura-idea-unlock">Book a call</a>
      </li>
    </ul>
  </nav>
</template>

<style scoped></style>
