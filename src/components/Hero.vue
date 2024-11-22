<script setup lang="ts">
const profile = {
  name: "Pratya Palee",
  title: "Full-Stack Developer",
  description:
    "I'm a full-stack developer focused on creating user-friendly programs and websites, committed to ongoing self-improvement and industry knowledge. I bring real-world experience and aim to drive your organization's rapid growth.",
  image: "../../public/profile/profile01-edit.png",
};
</script>

<template>
  <section
    id="about"
    class="min-h-screen flex items-center pt-16 bg-gradient-to-br from-blue-50 to-indigo-50"
  >
    <div class="container mx-auto px-4 py-16">
      <div class="flex flex-col md:flex-row items-center justify-between gap-8">
        <div class="md:w-1/2 text-center md:text-left">
          <h1 class="text-4xl md:text-6xl font-bold text-gray-900 mb-4">
            {{ profile.name }}
          </h1>
          <h2 class="text-2xl md:text-3xl text-blue-600 mb-6">
            {{ profile.title }}
          </h2>
          <p class="text-lg text-gray-600 mb-8">
            {{ profile.description }}
          </p>
          <a
            href="#contact"
            class="inline-block bg-blue-600 text-white px-8 py-3 rounded-lg hover:bg-blue-700 transition-colors"
          >
            Get in Touch
          </a>
        </div>
        <div class="md:w-1/2 flex justify-center">
          <img
            :src="profile.image"
            :alt="profile.name"
            class="rounded-full w-65 h-65 object-cover shadow-lg"
          />
        </div>
      </div>
    </div>
  </section>
</template>
