<script setup>
import { PhCheck } from "@phosphor-icons/vue";

const traditional = [
  "6 months of minimum development time",
  "$50,000+ for a basic MVP",
  "Hiring a team of Dev, QA, PM, Scrum ($100k+/year each)",
  "Many meetings and slow progress",
  "Fragmentation of the app architecture",
  "Security vulnerabilities",
  "Scalability issues as users grow",
  "Costly deployment with many services",
  "Managing hidden costs",
];

const ideaUnlock = [
  "MVP ready in 4 weeks",
  "Fixed price starting at $5,999",
  "Experienced team handles everything",
  "Weekly updates and rapid iterations",
  "Optimized, modern full stack (Laravel, React)",
  "Built in security",
  "Simple scalability",
  "24/7 tech support for 30 days post-launch",
  "Transparent pricing",
];
</script>

<template>
  <div class="banner-2 bg-white font-work_sans">
    <div class="width-content px-2 lg:px-8">
      <div class="mx-auto max-w-4xl text-center">
        <!--        <p class=" font-semibold text-pink-600">Hiring a team is expensive</p>-->
        <h2 class="heading2">Why IdeaUnlock?</h2>
      </div>

      <div
        class="isolate mx-auto mt-10 grid max-w-md grid-cols-1 gap-12 lg:mx-0 lg:max-w-7xl lg:grid-cols-2"
      >
        <!-- Traditional Approach -->
        <div class="card mx-auto flex w-full flex-col space-y-8 p-12">
          <h3 class="text-xl font-semibold text-gray-900">
            Traditional Software House
          </h3>
          <img
            class="w-72"
            alt="problem with building a mvp"
            src="../public/assets/problem.svg"
          />
          <ul class="space-y-4">
            <li
              v-for="(feature, index) in traditional"
              :key="index"
              class="flex items-center gap-x-3 text-gray-600"
            >
              <PhCheck :size="24" class="shrink-0 text-gray-400" />
              <span>{{ feature }}</span>
            </li>
          </ul>
        </div>

        <!-- With ideaUnlock -->
        <div class="card mx-auto flex w-full flex-col space-y-8 p-12">
          <h3 class="color-red text-xl font-semibold">With IdeaUnlock</h3>
          <img
            class="w-72"
            alt="problem with building a mvp"
            src="../public/assets/solution.svg"
          />
          <ul class="space-y-4">
            <li
              v-for="(feature, index) in ideaUnlock"
              :key="index"
              class="flex items-center gap-x-3 text-gray-600"
            >
              <PhCheck :size="24" class="color-red shrink-0" />
              <span>{{ feature }}</span>
            </li>
          </ul>
        </div>
      </div>
    </div>
  </div>
</template>
