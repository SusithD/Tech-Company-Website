<template>
  <section class="section-padding bg-white">
    <div class="container-custom">
      <div class="max-w-4xl mx-auto text-center mb-16">
        <h2 class="text-4xl md:text-5xl lg:text-6xl font-bold mb-6 text-gray-900">
          What We Enable
        </h2>
        <p class="text-xl text-gray-600 leading-relaxed">
          The future, engineered. We architect the technologies that redefine boundaries, 
          empower innovation, and unlock the next era of digital transformation.
        </p>
      </div>
      
      <div class="grid md:grid-cols-2 lg:grid-cols-3 gap-8">
        <div v-for="service in services" :key="service.title" 
             class="service-card bg-white p-8 rounded-2xl border border-gray-100 card-hover group">
          <div class="w-12 h-12 bg-gray-100 rounded-xl flex items-center justify-center mb-6 group-hover:bg-gray-900 transition-colors">
            <span class="text-2xl group-hover:text-white transition-colors">{{ service.icon }}</span>
          </div>
          <h3 class="text-xl font-bold mb-4 text-gray-900">
            {{ service.title }}
          </h3>
          <p class="text-gray-600 leading-relaxed">
            {{ service.description }}
          </p>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
import { onMounted } from 'vue'
import { gsap } from 'gsap'
import { ScrollTrigger } from 'gsap/ScrollTrigger'

const services = [
  {
    icon: '🚀',
    title: 'Digital Innovation',
    description: 'Transform your business with cutting-edge digital solutions that drive growth and efficiency.'
  },
  {
    icon: '🛡️',
    title: 'Cybersecurity',
    description: 'Protect your digital assets with enterprise-grade security solutions and monitoring.'
  },
  {
    icon: '☁️',
    title: 'Cloud Solutions',
    description: 'Migrate and optimize your infrastructure with scalable cloud technologies.'
  },
  {
    icon: '🤖',
    title: 'AI & Machine Learning',
    description: 'Harness the power of artificial intelligence to automate and optimize operations.'
  },
  {
    icon: '📱',
    title: 'Mobile Development',
    description: 'Create powerful mobile applications that engage users and drive business value.'
  },
  {
    icon: '⚡',
    title: 'Performance Optimization',
    description: 'Enhance system performance and reliability with advanced optimization techniques.'
  }
]

onMounted(() => {
  if (process.client) {
    gsap.registerPlugin(ScrollTrigger)
    
    gsap.fromTo('.service-card',
      { opacity: 0, y: 30 },
      {
        opacity: 1,
        y: 0,
        duration: 0.6,
        stagger: 0.1,
        ease: 'power3.out',
        scrollTrigger: {
          trigger: '.service-card',
          start: 'top 85%',
          toggleActions: 'play none none reverse'
        }
      }
    )
  }
})
</script>