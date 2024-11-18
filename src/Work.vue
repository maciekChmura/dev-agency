<script setup>
const apps = [
  {
    id: '1',
    name: 'Time Cube',
    description: 'Project management tool that helps architectural and construction designers streamline project tracking, manage teams, and control costs efficiently. It includes features like profitability forecasting, labor cost analysis, and leave management to improve office operations and project delivery.',
    link: 'https://timecube.app',
    image: '',
    status: 'closed',
    type: 'SaaS'
  },
  {
    id: '2',
    name: 'Patient Notes',
    description: 'AI-powered tool that streamlines medical documentation by transcribing consultations in real-time into clinical notes, summaries, and letters. It reduces administrative workload, offers customizable templates, and ensures data security while integrating seamlessly with practice management systems.',
    link: 'https://patientnotes.ai/',
    image: '',
    status: 'closed',
    type: 'AI app'
  },
  {
    id: '3',
    name: 'JobXDubai',
    description: 'Rapidly growing job board in the UAE, connecting job seekers with employers across various industries. The platform offers AI tools for HR, professional resume services, and one-on-one candidate consultations to streamline the recruitment process.',
    link: 'https://jobxdubai.com',
    image: '',
    status: 'closed',
    type: 'job board'
  },
  {
    id: '4',
    name: 'archipins',
    description: 'Specialized job board designed exclusively for architects and design professionals. It connects talent with leading firms, offering a curated selection of opportunities in architecture, urban planning, and interior design.',
    link: 'https://jobxdubai.com',
    image: '',
    status: 'closed',
    type: 'job board'

  },

]
</script>

<template>
  <div class="banner-3 space-y-10 pb-20" id="work">
    <h3 class="heading3 my-5">Recent MVP's</h3>
    <div class="card" v-for="app in apps" :key="app.id">
      <div class="space-y-5 py-8 px-8 md:py-16 md:px-20 md:w-1/2">
        <div class="flex flex-row justify-between">
          <h4 class="project-title item">{{ app.name }}</h4>
          <span
              class=" h-8 inline-flex items-center rounded-full bg-gray-50 px-4 py-0 text-sm font-medium text-gray-600 ring-1 ring-inset ring-gray-500/10">{{
              app.type
            }}</span>
        </div>
        <p class="font-work_sans pr-12">
          {{
            app.description
          }}
        </p>
        <button class="color-red  text-xl tracking-wider">
          <a :href="app.link" target="_blank">view project →</a>
        </button>
      </div>
      <div class="card-image bg-green-100">
        <img
            class="object-cover w-full h-72 md:h-96"
            src="./assets/project1.png"
        />
      </div>
    </div>
  </div>
</template>

<style scoped>

</style>