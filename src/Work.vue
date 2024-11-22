<script setup>
const apps = [
  {
    id: "1",
    name: "Time Cube",
    description:
      "Project management tool that helps architectural and construction designers streamline project tracking, manage teams, and control costs efficiently. It includes features like profitability forecasting, labor cost analysis, and leave management to improve office operations and project delivery.",
    link: "https://timecube.app",
    image: "./assets/timecube3.png",
    status: "closed",
    type: "SaaS",
  },
  {
    id: "2",
    name: "Patient Notes",
    description:
      "AI-powered tool that streamlines medical documentation by transcribing consultations in real-time into clinical notes, summaries, and letters. It reduces administrative workload, offers customizable templates, and ensures data security while integrating seamlessly with practice management systems.",
    link: "https://patientnotes.ai/",
    image: "./assets/patientnotes.png",
    status: "closed",
    type: "AI app",
  },
  {
    id: "3",
    name: "JobXDubai",
    description:
      "Rapidly growing job board in the UAE, connecting job seekers with employers across various industries. The platform offers AI tools for HR, professional resume services, and one-on-one candidate consultations to streamline the recruitment process.",
    link: "https://jobxdubai.com",
    image: "./assets/jobx.png",
    status: "closed",
    type: "job board",
  },
  {
    id: "4",
    name: "Archipins",
    description:
      "Specialized job board designed exclusively for architects and design professionals. It connects talent with leading firms, offering a curated selection of opportunities in architecture, urban planning, and interior design.",
    link: "",
    image: "./assets/archipins.png",
    status: "closed",
    type: "job board",
  },
];
</script>

<template>
  <div class="banner-1 width-content space-y-10 pb-20" id="work">
    <h3 class="heading2 my-16 text-center font-Eczar">Recent MVP's</h3>
    <div
      class="my-6 flex flex-col-reverse lg:flex-row"
      v-for="app in apps"
      :key="app.id"
    >
      <div class="space-y-8 py-8 px-8 lg:w-1/2 lg:py-16 lg:px-20">
        <div class="flex flex-row justify-between">
          <h4 class="project-title item text-[#FF4560]">{{ app.name }}</h4>
          <span
            class="inline-flex h-8 items-center rounded-full bg-red-50 px-4 py-0 text-sm font-medium text-red-600 ring-1 ring-inset ring-red-500/10"
            >{{ app.type }}</span
          >
        </div>
        <p class="text-pretty font-work_sans">
          {{ app.description }}
        </p>
        <button v-if="app.link" class="color-gray-700 text-xl tracking-wider">
          <a :href="app.link" target="_blank">view project →</a>
        </button>
      </div>
      <div class="my-auto object-cover lg:w-1/2">
        <img
          class="min-h-full transform rounded-2xl object-cover shadow-xl transition-transform duration-300 ease-in-out hover:-rotate-2 hover:scale-105"
          :src="app.image"
        />
      </div>
    </div>
  </div>
</template>

<style scoped></style>
