<script setup>
import { PhCheck } from "@phosphor-icons/vue";

const tiers = [
  {
    name: "Landing Page",
    id: "landing",
    price: "$999",
    description:
      "SEO-friendly, mobile-responsive landing pages to boost leads and interest in your MVP.",
    features: [
      "Custom built Landing page",
      "Custom domain",
      "Email waitlist",
      "SEO optimization",
      "Free hosting",
      "Analytics integration",
    ],
  },
  {
    name: "MVP",
    id: "mvp",
    price: "$5,999",
    description:
      "Turn your idea into a compelling MVP in weeks, ready to impress investors and early adopters.",
    features: [
      "Custom MVP development",
      "Core feature implementation",
      "User authentication",
      "Email integration",
      "Analytics integration",
      "Technical documentation",
      "30-day support",
    ],
  },
  {
    name: "MVP+",
    id: "custom",
    price: "Custom",
    description:
      "Full-featured solution with advanced capabilities and dedicated support.",
    features: [
      "Everything in MVP, plus:",
      "Multiple authentication options",
      "Custom integrations",
      "Performance optimization",
      "Scalable architecture",
      "Extended support package",
    ],
  },
];
</script>

<template>
  <div class="banner-1">
    <div class="width-content max-w-7xl px-6 lg:px-8">
      <div class="mx-auto max-w-4xl text-center">
        <h2 class="heading2">Simple pricing</h2>
      </div>
      <p
        class="sm:text-xl/8 mx-auto mt-6 max-w-2xl text-center text-lg font-medium"
      >
        100% custom MVP built for you
      </p>
      <div
        class="isolate mx-auto mt-10 grid max-w-md grid-cols-1 gap-8 lg:mx-auto lg:max-w-6xl lg:grid-cols-3"
      >
        <div
          v-for="tier in tiers"
          :key="tier.id"
          class="card flex flex-col rounded-xl border p-8"
        >
          <h3 :id="tier.id" class="font-Eczar text-3xl font-semibold">
            {{ tier.name }}
          </h3>
          <p class="text-sm/6 mt-4 h-20">{{ tier.description }}</p>
          <p class="mt-6 flex items-baseline gap-x-1">
            <span class="color-red text-4xl font-semibold tracking-tight">{{
              tier.price
            }}</span>
          </p>
          <ul
            role="list"
            class="text-sm/6 mt-8 w-full space-y-3 text-gray-700 xl:mt-10"
          >
            <li
              v-for="feature in tier.features"
              :key="feature"
              class="flex gap-x-3"
            >
              <PhCheck :size="24" class="shrink-0" />
              {{ feature }}
            </li>
          </ul>
        </div>
      </div>
    </div>
  </div>
</template>
