<script setup>
import { PhCheck } from "@phosphor-icons/vue";

const tiers = [
  {
    name: "MVP",
    id: "tier-mvp",
    price: "$5,999",
    description:
      "Perfect for validating your idea and getting to market quickly.",
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
    id: "tier-enterprise",
    price: "Custom",
    description:
      "Full-featured solution with advanced capabilities and dedicated support.",
    features: [
      "Everything in MVP, plus:",
      "Advanced security features",
      "Custom integrations",
      "Performance optimization",
      "Scalable architecture",
      "Extended support package",
    ],
  },
];
</script>

<template>
  <div class="baner-1 py-24 sm:py-32">
    <div class="mx-auto max-w-7xl px-6 lg:px-8">
      <div class="mx-auto max-w-4xl text-center">
        <h2 class="text-balance mt-2 text-5xl tracking-tight sm:text-6xl">
          Simple pricing
        </h2>
      </div>
      <p
        class="sm:text-xl/8 mx-auto mt-6 max-w-2xl text-center text-lg font-medium"
      >
        100% custom MVP built for you
      </p>
      <div
        class="isolate mx-auto mt-10 grid max-w-md grid-cols-1 gap-8 lg:mx-auto lg:max-w-4xl lg:grid-cols-2"
      >
        <div
          v-for="tier in tiers"
          :key="tier.id"
          class="card flex flex-col rounded-xl border p-8"
        >
          <h3 :id="tier.id" class="font-Eczar text-3xl font-semibold">
            {{ tier.name }}
          </h3>
          <p class="text-sm/6 mt-4">{{ tier.description }}</p>
          <p class="mt-6 flex items-baseline gap-x-1">
            <span class="color-red text-4xl font-semibold tracking-tight">{{
              tier.price
            }}</span>
          </p>
          <ul
            role="list"
            class="text-sm/6 mt-8 space-y-3 text-gray-700 xl:mt-10"
          >
            <li
              v-for="feature in tier.features"
              :key="feature"
              class="flex gap-x-3"
            >
              <PhCheck :size="24" />
              {{ feature }}
            </li>
          </ul>
        </div>
      </div>
    </div>
  </div>
</template>
