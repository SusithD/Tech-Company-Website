<template>
  <section class="py-16 bg-white border-b border-gray-100">
    <div class="container-custom">
      <div class="text-center mb-12">
        <p class="text-gray-500 font-medium mb-8">Trusted by 500+ global companies</p>
      </div>
      
      <div class="grid grid-cols-3 md:grid-cols-6 lg:grid-cols-8 gap-8 items-center justify-items-center opacity-60">
        <div v-for="company in companies" :key="company.name" 
             class="company-logo flex items-center justify-center h-12 transition-opacity hover:opacity-100">
          <span class="text-2xl font-bold text-gray-400">{{ company.logo }}</span>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
const companies = [
  { name: 'Microsoft', logo: 'Microsoft' },
  { name: 'Google', logo: 'Google' },
  { name: 'Amazon', logo: 'Amazon' },
  { name: 'Apple', logo: 'Apple' },
  { name: 'Meta', logo: 'Meta' },
  { name: 'Netflix', logo: 'Netflix' },
  { name: 'Spotify', logo: 'Spotify' },
  { name: 'Adobe', logo: 'Adobe' }
]
</script>