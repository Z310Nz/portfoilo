<script setup lang="ts">
const contact = {
  email: "pratya.palee@gmail.com",
  phone: "+66 0984808453",
  location:
    "1 Village No. 6, Sri Don Chai Subdistrict, Thoeng District, Chiang Rai Province, Thailand 57230",
  social: [
    { name: "GitHub", url: "https://github.com/Z310Nz" },
    {
      name: "LinkedIn",
      url: "https://bit.ly/Linkedin-ppalee",
    },
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
              <p class="flex">
                <span class="w-5 h-5 mr-3">📍</span>
                {{ contact.location }}
              </p>
            </div>
          </div>

          <div class="bg-white p-6 rounded-lg shadow-sm mt-6">
            <ul class="space-y-4">
              <li
                v-for="link in contact.social"
                :key="link.name"
                class="flex items-start"
              >
                <span class="text-blue-600 mr-3">🔗</span>
                <span
                  >{{ link.name }} :
                  <a :href="link.url" target="_blank" class="text-blue-600">
                    {{ link.url }}
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
