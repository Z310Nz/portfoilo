<script setup lang="ts">
const experiences = [
  {
    title: 'Senior Full-Stack Developer',
    company: 'Tech Corp',
    period: '2020 - Present',
    description: 'Led development of enterprise applications using Vue.js and Node.js. Managed team of 5 developers.',
  },
  {
    title: 'Full-Stack Developer',
    company: 'Digital Solutions Inc',
    period: '2018 - 2020',
    description: 'Developed and maintained multiple web applications. Implemented CI/CD pipelines.',
  },
  {
    title: 'Junior Developer',
    company: 'StartUp Hub',
    period: '2016 - 2018',
    description: 'Worked on front-end development using React and Vue.js. Collaborated with UX team.',
  },
];

const awards = [
  'Best Innovation Award 2023',
  'Employee of the Year 2022',
  'Outstanding Performance 2021',
];
</script>

<template>
  <section id="experience" class="py-20 bg-gray-50">
    <div class="container mx-auto px-4">
      <h2 class="text-3xl font-bold text-center mb-12">Experience & Achievements</h2>
      
      <div class="grid md:grid-cols-3 gap-8">
        <!-- Work History -->
        <div class="md:col-span-2">
          <h3 class="text-xl font-semibold mb-6">Work History</h3>
          <div class="space-y-8">
            <div v-for="exp in experiences" 
                 :key="exp.title"
                 class="bg-white p-6 rounded-lg shadow-sm">
              <h4 class="text-lg font-semibold text-gray-900">{{ exp.title }}</h4>
              <p class="text-blue-600">{{ exp.company }}</p>
              <p class="text-sm text-gray-500 mb-3">{{ exp.period }}</p>
              <p class="text-gray-600">{{ exp.description }}</p>
            </div>
          </div>
        </div>

        <!-- Awards -->
        <div>
          <h3 class="text-xl font-semibold mb-6">Awards & Achievements</h3>
          <div class="bg-white p-6 rounded-lg shadow-sm">
            <ul class="space-y-4">
              <li v-for="award in awards" 
                  :key="award"
                  class="flex items-start">
                <span class="text-blue-600 mr-3">🏆</span>
                <span>{{ award }}</span>
              </li>
            </ul>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>