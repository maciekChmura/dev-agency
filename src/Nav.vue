<script setup>

</script>

<template>
  <nav
      class="container px-6 mx-auto md:flex md:justify-between md:items-center"
  >
    <div class="flex items-center justify-between">
      <div class="relative mr-4">
        <!--          <img-->
        <!--            class="rounded-full border border-gray-100 shadow-sm"-->
        <!--            src="https://images.unsplash.com/photo-1531746020798-e6953c6e8e04?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=512&h=512&q=80"-->
        <!--            alt="user image"-->
        <!--          />-->
        <img class="h-20" src="./assets/logo.svg" alt="logo"/>
      </div>
      <div class="text-3xl hidden lg:block text-gray-900 font-Eczar font-bold">ideaUnlock</div>
      <!-- Mobile menu button -->
      <div @click="showMenu = !showMenu" class="flex md:hidden">
        <button
            type="button"
            class="text-gray-800 hover:text-gray-400 focus:outline-none focus:text-gray-400"
        >
          <svg viewBox="0 0 24 24" class="w-6 h-6 fill-current">
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
        class="flex-col items-end mt-8 space-y-4 md:flex md:space-y-0 md:flex-row md:items-center md:space-x-10 md:mt-0"
    >
      <li class="menu-button"><a href="#">Home</a></li>
      <li class="menu-button"><a href="#work" v-smooth-scroll>Works</a></li>
      <!--      <li class="menu-button">-->
      <!--        <a href="#testimonial" v-smooth-scroll>Testimonials</a>-->
      <!--      </li>-->
      <li class="menu-button"><a href="#about" v-smooth-scroll>About</a></li>
    </ul>
  </nav>
</template>

<style scoped>

</style>