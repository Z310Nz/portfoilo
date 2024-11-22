<script setup lang="ts">
const profile = {
  name: 'John Doe',
  title: 'Full-Stack Developer',
  description: 'Passionate developer with expertise in building scalable web applications using modern technologies.',
  image: 'https://via.placeholder.com/150',
};
</script>

<template>
  <section class="min-h-screen flex items-center pt-16 bg-gradient-to-br from-blue-50 to-indigo-50">
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
          <a href="#contact" 
             class="inline-block bg-blue-600 text-white px-8 py-3 rounded-lg hover:bg-blue-700 transition-colors">
            Get in Touch
          </a>
        </div>
        <div class="md:w-1/2 flex justify-center">
          <img :src="profile.image" 
               :alt="profile.name"
               class="rounded-full w-64 h-64 object-cover shadow-lg" />
        </div>
      </div>
    </div>
  </section>
</template>