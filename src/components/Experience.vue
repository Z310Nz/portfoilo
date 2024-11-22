<script setup lang="ts">
const experiences = [
  {
    title: "Back-end Developer - internship",
    company: "CODIUM",
    period: "April 2024 - September 2024",
    description:
      "Developed and maintained E-Tax projects, including designing UX/UI for new project versions, adding the Billing Feature for the Standard V.2 Project, implementing features based on customer requirements, fixing system-related bugs, managing servers, and investigating errors to improve system stability and functionality.",
  },
  {
    title: "Full-Stack Developer",
    company: "University of Phayao",
    period: "November 2023 - February 2024",
    description:
      "Develop a website for internship applications for software engineering students in various positions, with 3 groups of users: companies that want to hire students for internships, students who want to submit internship applications to companies, and instructors who check the status of each student.",
  },
  {
    title: "Back-end Developer",
    company: "INBOX Corporation Co., Ltd.",
    period: "July 2023 - October 2023",
    description:
      "Worked on front-end development using React and Vue.js. Collaborated with UX team.",
  },
  {
    title: "Back-end Developer - internship",
    company: "CODIUM",
    period: "April 2023 - May 2023",
    description:
      "Developed and enhanced E-Tax projects by designing UX/UI for new project versions, adding features based on customer needs, resolving system-related bugs, and investigating unknown errors to improve functionality and user experience.",
  },
];

const awards = [
  "1ts place of the PM/Tester/QA Award In presenting student internship project 2024",
  "3rd place of the mobile Application Award In presenting student project, 2023",
  "Honorable Mention prize of the Web Application Award In presenting student internship project, 2023",
];

const work = [
  { name: "MonopolyHistoryGame", url: "https://monopoly-history.vercel.app/" },
  { name: "SEinternship", url: "https://seinternship.cstserver.org/" },
  { name: "SEinternship Repository", url: "https://bit.ly/seinternweb" },
];
</script>

<template>
  <section id="experience" class="py-20 bg-gray-50">
    <div class="container mx-auto px-4">
      <h2 class="text-3xl font-bold text-center mb-12">
        Experience & Achievements
      </h2>

      <div class="grid md:grid-cols-3 gap-8">
        <!-- Work History -->
        <div class="md:col-span-2">
          <h3 class="text-xl font-semibold mb-6">Work History</h3>
          <div class="space-y-8">
            <div
              v-for="exp in experiences"
              :key="exp.title"
              class="bg-white p-6 rounded-lg shadow-sm"
            >
              <h4 class="text-lg font-semibold text-gray-900">
                {{ exp.title }}
              </h4>
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
              <li v-for="award in awards" :key="award" class="flex items-start">
                <span class="text-blue-600 mr-3">🏆</span>
                <span>{{ award }}</span>
              </li>
            </ul>
          </div>
          <div class="bg-white p-6 rounded-lg shadow-sm mt-6">
            <ul class="space-y-4">
              <li
                v-for="work in work"
                :key="work.name"
                class="flex items-start"
              >
                <span class="text-blue-600 mr-3">🔗</span>
                <span
                  >{{ work.name }} :
                  <a :href="work.url" target="_blank" class="text-blue-600">
                    {{ work.url }}
                  </a>
                </span>
              </li>
            </ul>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>
