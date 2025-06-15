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
            <div class="w-8 h-8 mx-auto mb-3 flex items-center justify-center">
              <component :is="platform.icon" class="w-6 h-6 text-gray-600 group-hover:text-gray-900 transition-colors" />
            </div>
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
import {
  WindowIcon,
  CodeBracketIcon,
  CubeIcon,
  DevicePhoneMobileIcon,
  CircleStackIcon,
  CommandLineIcon,
  CloudIcon,
  ServerIcon,
  CpuChipIcon,
  AtSymbolIcon,
  CircleStackIcon as DatabaseIcon,
  RocketLaunchIcon
} from '@heroicons/vue/24/outline'

const platforms = [
  { name: 'Microsoft', icon: WindowIcon },
  { name: 'C#', icon: CodeBracketIcon },
  { name: 'Kotlin', icon: CubeIcon },
  { name: 'Android', icon: DevicePhoneMobileIcon },
  { name: 'SQL', icon: CircleStackIcon },
  { name: 'JavaScript', icon: CommandLineIcon },
  { name: 'AWS', icon: CloudIcon },
  { name: 'Azure', icon: ServerIcon },
  { name: 'Docker', icon: CubeIcon },
  { name: 'React', icon: AtSymbolIcon },
  { name: 'Node.js', icon: ServerIcon },
  { name: 'Python', icon: RocketLaunchIcon }
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