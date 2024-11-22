<script setup lang="ts">
import { ref } from "vue";
import { Bars3Icon, XMarkIcon } from "@heroicons/vue/24/outline";

const isMenuOpen = ref(false);

const navigation = [
  { name: "About", href: "#about" },
  { name: "Skills", href: "#skills" },
  { name: "Experience", href: "#experience" },
  { name: "Contact", href: "#contact" },
];
</script>

<template>
  <header class="fixed w-full bg-white shadow-sm z-50">
    <nav class="container mx-auto px-4 py-4">
      <div class="flex items-center justify-between">
        <div class="text-2xl font-bold text-gray-800">Portfolio</div>

        <!-- Desktop Navigation -->
        <div class="hidden md:flex space-x-8">
          <a
            v-for="item in navigation"
            :key="item.name"
            :href="item.href"
            class="text-gray-600 hover:text-gray-900 transition-colors"
          >
            {{ item.name }}
          </a>
        </div>

        <!-- Mobile Navigation Button -->
        <button @click="isMenuOpen = !isMenuOpen" class="md:hidden">
          <Bars3Icon v-if="!isMenuOpen" class="h-6 w-6" />
          <XMarkIcon v-else class="h-6 w-6" />
        </button>
      </div>

      <!-- Mobile Navigation Menu -->
      <div v-if="isMenuOpen" class="md:hidden mt-4 space-y-2">
        <a
          v-for="item in navigation"
          :key="item.name"
          :href="item.href"
          @click="isMenuOpen = false"
          class="block py-2 text-gray-600 hover:text-gray-900 transition-colors"
        >
          {{ item.name }}
        </a>
      </div>
    </nav>
  </header>
</template>
