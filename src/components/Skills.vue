<script setup lang="ts">
const skills = {
  technical: [
    "Python",
    "PHP",
    "TypeScript",
    "JavaScript",
    "Node.js",
    "MySQL",
    "Django",
    "AngularTS",
    "VueJS",
    "Laravel",
    "Bootstrap",
  ],
  soft: [
    "Problem Solving",
    "Team Leadership",
    "Communication",
    "Time Management",
    "Adaptability",
    "Quick to learn",
    "Detail-oriented",
    "Problem solving",
    "Critical thinking",
    "Flexibility",
    "Teamwork",
    "Creativity",
  ],
  tools: [
    "VS Code",
    "Git",
    "GitHub",
    "GitLab",
    "Docker",
    "Postman",
    "Teleport",
  ],
  languages: [
    "Writing : Well",
    "listening : Good",
    "Speaking : Well",
    "Reading : Good",
  ],
};
</script>

<template>
  <section id="skills" class="py-20 bg-white">
    <div class="container mx-auto px-4">
      <h2 class="text-3xl font-bold text-center mb-12">Skills & Expertise</h2>

      <div class="grid md:grid-cols-4 gap-8">
        <!-- Technical Skills -->
        <div class="bg-gray-50 p-6 rounded-lg">
          <h3 class="text-xl font-semibold mb-6">Technical Skills</h3>
          <ul class="space-y-4">
            <li
              v-for="skill in skills.technical"
              :key="skill"
              class="flex items-center"
            >
              <span class="w-2 h-2 bg-blue-600 rounded-full mr-3"></span>
              {{ skill }}
            </li>
          </ul>
        </div>

        <!-- Soft Skills -->
        <div class="bg-gray-50 p-6 rounded-lg">
          <h3 class="text-xl font-semibold mb-6">Soft Skills</h3>
          <ul class="space-y-3">
            <li
              v-for="skill in skills.soft"
              :key="skill"
              class="flex items-center"
            >
              <span class="w-2 h-2 bg-blue-600 rounded-full mr-3"></span>
              {{ skill }}
            </li>
          </ul>
        </div>

        <!-- Tools -->
        <div class="bg-gray-50 p-6 rounded-lg">
          <h3 class="text-xl font-semibold mb-6">Tools & Technologies</h3>
          <ul class="space-y-3">
            <li
              v-for="tool in skills.tools"
              :key="tool"
              class="flex items-center"
            >
              <span class="w-2 h-2 bg-blue-600 rounded-full mr-3"></span>
              {{ tool }}
            </li>
          </ul>
        </div>

        <!-- Languages Skills -->
        <div class="bg-gray-50 p-6 rounded-lg">
          <h3 class="text-xl font-semibold mb-6">English Skills</h3>
          <ul class="space-y-3">
            <li
              v-for="skill in skills.languages"
              :key="skill"
              class="flex items-center"
            >
              <span class="w-2 h-2 bg-blue-600 rounded-full mr-3"></span>
              {{ skill }}
            </li>
          </ul>
        </div>
      </div>
    </div>
  </section>
</template>
