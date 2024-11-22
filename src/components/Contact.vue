<script setup lang="ts">
const contact = {
  email: 'john.doe@example.com',
  phone: '+1 (555) 123-4567',
  location: 'San Francisco, CA',
  social: [
    { name: 'GitHub', url: 'https://github.com' },
    { name: 'LinkedIn', url: 'https://linkedin.com' },
    { name: 'Twitter', url: 'https://twitter.com' },
  ],
};
</script>

<template>
  <section id="contact" class="py-20 bg-white">
    <div class="container mx-auto px-4">
      <h2 class="text-3xl font-bold text-center mb-12">Get in Touch</h2>
      
      <div class="max-w-2xl mx-auto bg-gray-50 rounded-lg p-8">
        <div class="grid md:grid-cols-2 gap-8">
          <div>
            <h3 class="text-xl font-semibold mb-4">Contact Information</h3>
            <div class="space-y-4">
              <p class="flex items-center">
                <span class="w-5 h-5 mr-3">📧</span>
                {{ contact.email }}
              </p>
              <p class="flex items-center">
                <span class="w-5 h-5 mr-3">📱</span>
                {{ contact.phone }}
              </p>
              <p class="flex items-center">
                <span class="w-5 h-5 mr-3">📍</span>
                {{ contact.location }}
              </p>
            </div>
          </div>
          
          <div>
            <h3 class="text-xl font-semibold mb-4">Social Links</h3>
            <div class="space-y-4">
              <a v-for="link in contact.social" 
                 :key="link.name"
                 :href="link.url"
                 target="_blank"
                 class="flex items-center text-blue-600 hover:text-blue-700 transition-colors">
                <span class="w-5 h-5 mr-3">🔗</span>
                {{ link.name }}
              </a>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>