<script setup lang="ts">
const skills = {
  technical: [
    { name: 'JavaScript/TypeScript', level: 90 },
    { name: 'Vue.js/React', level: 85 },
    { name: 'Node.js', level: 80 },
    { name: 'Python', level: 75 },
    { name: 'SQL/NoSQL', level: 85 },
  ],
  soft: [
    'Problem Solving',
    'Team Leadership',
    'Communication',
    'Project Management',
    'Agile Methodologies',
  ],
  tools: [
    'VS Code',
    'Git',
    'Docker',
    'AWS',
    'Jira',
  ],
};
</script>

<template>
  <section id="skills" class="py-20 bg-white">
    <div class="container mx-auto px-4">
      <h2 class="text-3xl font-bold text-center mb-12">Skills & Expertise</h2>
      
      <div class="grid md:grid-cols-3 gap-8">
        <!-- Technical Skills -->
        <div class="bg-gray-50 p-6 rounded-lg">
          <h3 class="text-xl font-semibold mb-6">Technical Skills</h3>
          <div class="space-y-4">
            <div v-for="skill in skills.technical" :key="skill.name">
              <div class="flex justify-between mb-1">
                <span>{{ skill.name }}</span>
                <span>{{ skill.level }}%</span>
              </div>
              <div class="w-full bg-gray-200 rounded-full h-2">
                <div class="bg-blue-600 h-2 rounded-full" 
                     :style="{ width: `${skill.level}%` }"></div>
              </div>
            </div>
          </div>
        </div>

        <!-- Soft Skills -->
        <div class="bg-gray-50 p-6 rounded-lg">
          <h3 class="text-xl font-semibold mb-6">Soft Skills</h3>
          <ul class="space-y-3">
            <li v-for="skill in skills.soft" 
                :key="skill"
                class="flex items-center">
              <span class="w-2 h-2 bg-blue-600 rounded-full mr-3"></span>
              {{ skill }}
            </li>
          </ul>
        </div>

        <!-- Tools -->
        <div class="bg-gray-50 p-6 rounded-lg">
          <h3 class="text-xl font-semibold mb-6">Tools & Technologies</h3>
          <ul class="space-y-3">
            <li v-for="tool in skills.tools" 
                :key="tool"
                class="flex items-center">
              <span class="w-2 h-2 bg-blue-600 rounded-full mr-3"></span>
              {{ tool }}
            </li>
          </ul>
        </div>
      </div>
    </div>
  </section>
</template>