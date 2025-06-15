<template>
  <section class="section-padding bg-gray-50">
    <div class="container-custom">
      <div class="text-center mb-16">
        <h2 class="text-4xl md:text-5xl font-bold mb-6 text-gray-900">
          Working with
        </h2>
        <p class="text-xl text-gray-600 max-w-3xl mx-auto">
          Drive digital transformation across your organization with our specialized knowledge 
          of key software and platforms.
        </p>
      </div>
      
      <div class="platforms-section">
        <h3 class="text-2xl font-bold text-center mb-8 text-gray-900">Platforms</h3>
        <div class="grid grid-cols-3 md:grid-cols-4 lg:grid-cols-6 gap-6">
          <div v-for="platform in platforms" :key="platform.name" 
               class="platform-item bg-white p-6 rounded-xl text-center card-hover group border border-gray-100">
            <div class="text-3xl mb-2">{{ platform.icon }}</div>
            <span class="text-sm font-medium text-gray-600 group-hover:text-gray-900 transition-colors">
              {{ platform.name }}
            </span>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
import { onMounted } from 'vue'
import { gsap } from 'gsap'
import { ScrollTrigger } from 'gsap/ScrollTrigger'

const platforms = [
  { name: 'Microsoft', icon: '⊞' },
  { name: 'C#', icon: '©' },
  { name: 'Kotlin', icon: '🔷' },
  { name: 'Android', icon: '🤖' },
  { name: 'SQL', icon: '💾' },
  { name: 'JavaScript', icon: '📟' },
  { name: 'AWS', icon: '☁' },
  { name: 'Azure', icon: '🔷' },
  { name: 'Docker', icon: '🐳' },
  { name: 'React', icon: '⚛' },
  { name: 'Node.js', icon: '🟢' },
  { name: 'Python', icon: '🐍' }
]

onMounted(() => {
  if (process.client) {
    gsap.registerPlugin(ScrollTrigger)
    
    gsap.fromTo('.platform-item',
      { opacity: 0, y: 20 },
      {
        opacity: 1,
        y: 0,
        duration: 0.5,
        stagger: 0.05,
        ease: 'power3.out',
        scrollTrigger: {
          trigger: '.platforms-section',
          start: 'top 80%',
          toggleActions: 'play none none reverse'
        }
      }
    )
  }
})
</script>