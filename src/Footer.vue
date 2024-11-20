<script setup>
import { computed } from "vue";

const currentYear = computed(() => new Date().getFullYear());
</script>

<template>
  <div class="h-12 border-t border-gray-100">
    <div class="container mx-auto px-6 py-8">
      <!-- Main Footer Content -->
      <div class="flex flex-col items-center justify-center space-y-6">
        <!-- Logo and Brand -->
        <div class="flex items-center space-x-4">
          <img class="h-12" src="./assets/logo.svg" alt="logo" />
          <div class="font-Eczar text-xl font-bold text-gray-900">
            ideaUnlock
          </div>
        </div>

        <!-- Navigation Links -->
        <nav>
          <ul class="flex flex-wrap items-center justify-center space-x-8">
            <li>
              <a href="#" class="text-gray-600 hover:text-gray-900">Home</a>
            </li>
            <li>
              <a href="#work" class="text-gray-600 hover:text-gray-900"
                >Works</a
              >
            </li>
            <li>
              <a href="#about" class="text-gray-600 hover:text-gray-900"
                >About</a
              >
            </li>
            <!--            <li>-->
            <!--              <a href="#call" class="text-gray-600 hover:text-gray-900"-->
            <!--                >Book a call</a-->
            <!--              >-->
            <!--            </li>-->
          </ul>
        </nav>

        <!-- Copyright -->
        <div class="text-sm text-gray-500">
          © {{ currentYear }} ideaUnlock. All rights reserved.
        </div>
      </div>
    </div>
  </div>
</template>
