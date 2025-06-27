<template>
  <section class="section-padding bg-gradient-to-br from-gray-50 via-white to-gray-50 relative overflow-hidden">
    <!-- Background Pattern -->
    <div class="absolute inset-0 opacity-5">
      <div class="absolute inset-0" style="background-image: radial-gradient(circle at 25% 75%, rgba(59, 130, 246, 0.1) 0%, transparent 50%), radial-gradient(circle at 75% 25%, rgba(147, 51, 234, 0.1) 0%, transparent 50%);"></div>
    </div>

    <div class="container-custom relative z-10">
      <!-- Achievements Section -->
      <div class="mb-32">
        <!-- Header -->
        <div class="max-w-4xl mx-auto text-center mb-20">
          <div class="inline-flex items-center bg-yellow-100 text-yellow-800 px-6 py-3 rounded-full text-sm font-semibold mb-8">
            <span class="w-2 h-2 bg-yellow-500 rounded-full mr-3"></span>
            ACHIEVEMENTS & RECOGNITION
          </div>
          
          <h2 class="text-5xl md:text-6xl lg:text-7xl font-bold mb-8 text-gray-900 font-heading leading-tight">
            Industry
            <span class="block gradient-text animate-gradient">Recognition</span>
            <span class="block text-4xl md:text-5xl lg:text-6xl text-gray-700">& Awards</span>
          </h2>
          
          <p class="text-xl text-gray-600 leading-relaxed">
            Our commitment to excellence has been recognized by industry leaders and prestigious organizations worldwide.
          </p>
        </div>

        <!-- Awards Grid -->
        <div class="grid md:grid-cols-2 lg:grid-cols-3 gap-8 mb-16">
          <div v-for="(award, index) in awards" :key="award.title"
               class="award-card group relative bg-white p-8 rounded-3xl border border-gray-200 hover:border-yellow-300 transition-all duration-500 cursor-pointer overflow-hidden">
            
            <div class="absolute inset-0 bg-gradient-to-br from-yellow-50 to-orange-50 opacity-0 group-hover:opacity-100 transition-opacity duration-500"></div>
            
            <div class="relative z-10 text-center">
              <div :class="award.iconClass" class="w-16 h-16 rounded-2xl flex items-center justify-center mx-auto mb-6 group-hover:scale-110 transition-transform duration-500">
                <component :is="award.icon" class="w-8 h-8 text-white" />
              </div>
              
              <h3 class="text-xl font-bold mb-3 text-gray-900 group-hover:text-yellow-900 transition-colors duration-300">
                {{ award.title }}
              </h3>
              
              <div class="text-yellow-600 font-semibold mb-3">{{ award.organization }}</div>
              <div class="text-gray-500 text-sm mb-4">{{ award.year }}</div>
              
              <p class="text-gray-600 leading-relaxed group-hover:text-gray-700 transition-colors duration-300">
                {{ award.description }}
              </p>
            </div>
          </div>
        </div>

        <!-- Certifications -->
        <div class="bg-white p-12 rounded-3xl border border-gray-200">
          <div class="text-center mb-12">
            <h3 class="text-3xl font-bold mb-4 text-gray-900 font-heading">Certifications & Partnerships</h3>
            <p class="text-gray-600">Industry-leading certifications and strategic partnerships that ensure the highest standards</p>
          </div>
          
          <div class="grid grid-cols-2 md:grid-cols-4 gap-8">
            <div v-for="cert in certifications" :key="cert.name" class="cert-item text-center group cursor-pointer">
              <div class="w-16 h-16 bg-gray-100 rounded-xl flex items-center justify-center mx-auto mb-4 group-hover:bg-blue-100 transition-colors duration-300">
                <span class="text-2xl font-bold text-gray-600 group-hover:text-blue-600 transition-colors duration-300">{{ cert.icon }}</span>
              </div>
              <h4 class="font-semibold text-gray-900 mb-1">{{ cert.name }}</h4>
              <div class="text-sm text-gray-500">{{ cert.type }}</div>
            </div>
          </div>
        </div>
      </div>

      <!-- Culture Section -->
      <div>
        <!-- Header -->
        <div class="max-w-4xl mx-auto text-center mb-20">
          <div class="inline-flex items-center bg-purple-100 text-purple-800 px-6 py-3 rounded-full text-sm font-semibold mb-8">
            <span class="w-2 h-2 bg-purple-500 rounded-full mr-3"></span>
            COMPANY CULTURE
          </div>
          
          <h2 class="text-5xl md:text-6xl lg:text-7xl font-bold mb-8 text-gray-900 font-heading leading-tight">
            Life at
            <span class="block gradient-text animate-gradient">MB Tech</span>
            <span class="block text-4xl md:text-5xl lg:text-6xl text-gray-700">Now</span>
          </h2>
          
          <p class="text-xl text-gray-600 leading-relaxed">
            We've built more than a company – we've created a community of innovators, dreamers, and builders 
            who are passionate about transforming the world through technology.
          </p>
        </div>

        <!-- Culture Highlights -->
        <div class="grid lg:grid-cols-2 gap-16 items-center mb-20">
          <!-- Content -->
          <div class="culture-content">
            <h3 class="text-3xl font-bold mb-6 text-gray-900 font-heading">Where Innovation Meets Purpose</h3>
            
            <div class="space-y-6 text-lg text-gray-600 leading-relaxed">
              <p>
                At MB Tech Now, we believe that <span class="font-semibold text-gray-800">great technology comes from great people</span>. 
                Our culture is built on collaboration, continuous learning, and the shared mission to make a meaningful impact 
                through digital transformation.
              </p>
              
              <p>
                We foster an environment where <span class="font-semibold text-gray-800">creativity flourishes</span>, where team members 
                are encouraged to take ownership, experiment with new ideas, and grow both personally and professionally.
              </p>
            </div>
            
            <!-- Culture Stats -->
            <div class="grid grid-cols-2 gap-6 mt-12">
              <div class="culture-stat-item p-6 bg-gray-50 rounded-2xl">
                <div class="text-3xl font-bold text-purple-600 mb-2 counter" data-target="95">0</div>
                <div class="text-gray-700 font-medium">Employee Satisfaction</div>
              </div>
              <div class="culture-stat-item p-6 bg-gray-50 rounded-2xl">
                <div class="text-3xl font-bold text-blue-600 mb-2 counter" data-target="92">0</div>
                <div class="text-gray-700 font-medium">Retention Rate</div>
              </div>
              <div class="culture-stat-item p-6 bg-gray-50 rounded-2xl">
                <div class="text-3xl font-bold text-green-600 mb-2 counter" data-target="40">0</div>
                <div class="text-gray-700 font-medium">Hours/Week Learning</div>
              </div>
              <div class="culture-stat-item p-6 bg-gray-50 rounded-2xl">
                <div class="text-3xl font-bold text-orange-600 mb-2 counter" data-target="25">0</div>
                <div class="text-gray-700 font-medium">Countries Represented</div>
              </div>
            </div>
          </div>
          
          <!-- Visual -->
          <div class="culture-visual">
            <div class="bg-white p-8 rounded-3xl border border-gray-200 shadow-lg">
              <div class="aspect-w-16 aspect-h-12 bg-gradient-to-br from-purple-100 to-blue-100 rounded-2xl mb-6 flex items-center justify-center">
                <div class="text-center">
                  <div class="w-20 h-20 bg-gray-900 rounded-2xl flex items-center justify-center mx-auto mb-4">
                    <svg class="w-10 h-10 text-white" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                      <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4.318 6.318a4.5 4.5 0 000 6.364L12 20.364l7.682-7.682a4.5 4.5 0 00-6.364-6.364L12 7.636l-1.318-1.318a4.5 4.5 0 00-6.364 0z"></path>
                    </svg>
                  </div>
                  <div class="text-gray-700 font-semibold">Our Team</div>
                </div>
              </div>
              
              <div class="text-center">
                <h4 class="text-xl font-bold text-gray-900 mb-4">Join Our Mission</h4>
                <p class="text-gray-600 mb-6">Be part of a team that's shaping the future of enterprise technology</p>
                <button class="inline-flex items-center bg-purple-600 text-white px-6 py-3 rounded-full font-semibold hover:bg-purple-700 transition-colors duration-300">
                  <span>View Open Positions</span>
                  <svg class="w-4 h-4 ml-2" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M17 8l4 4m0 0l-4 4m4-4H3"></path>
                  </svg>
                </button>
              </div>
            </div>
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
  TrophyIcon,
  StarIcon,
  ShieldCheckIcon,
  BoltIcon,
  GlobeAltIcon,
  CpuChipIcon
} from '@heroicons/vue/24/outline'

const awards = [
  {
    title: 'Digital Transformation Company of the Year',
    organization: 'Tech Excellence Awards',
    year: '2024',
    icon: TrophyIcon,
    iconClass: 'bg-gradient-to-r from-yellow-500 to-orange-500',
    description: 'Recognized for outstanding innovation in enterprise digital transformation solutions.'
  },
  {
    title: 'Best Enterprise AI Implementation',
    organization: 'AI Innovation Summit',
    year: '2023',
    icon: CpuChipIcon,
    iconClass: 'bg-gradient-to-r from-blue-500 to-purple-500',
    description: 'Awarded for pioneering AI-first approaches in enterprise transformation.'
  },
  {
    title: 'Cybersecurity Excellence Award',
    organization: 'Security Leaders Forum',
    year: '2023',
    icon: ShieldCheckIcon,
    iconClass: 'bg-gradient-to-r from-green-500 to-teal-500',
    description: 'Honored for maintaining zero security breaches and implementing best practices.'
  },
  {
    title: 'Global Technology Partner',
    organization: 'Microsoft Partner Awards',
    year: '2022',
    icon: GlobeAltIcon,
    iconClass: 'bg-gradient-to-r from-indigo-500 to-blue-500',
    description: 'Recognized as a leading global partner for cloud transformation services.'
  },
  {
    title: 'Innovation in Cloud Services',
    organization: 'Cloud Computing Awards',
    year: '2022',
    icon: BoltIcon,
    iconClass: 'bg-gradient-to-r from-purple-500 to-pink-500',
    description: 'Celebrated for innovative cloud migration and optimization solutions.'
  },
  {
    title: 'Client Satisfaction Excellence',
    organization: 'Business Excellence Institute',
    year: '2021',
    icon: StarIcon,
    iconClass: 'bg-gradient-to-r from-orange-500 to-red-500',
    description: 'Achieved 98% client satisfaction rate across all enterprise projects.'
  }
]

const certifications = [
  { name: 'ISO 27001', type: 'Security', icon: '🔒' },
  { name: 'AWS Partner', type: 'Cloud', icon: '☁️' },
  { name: 'Microsoft Gold', type: 'Partnership', icon: '🥇' },
  { name: 'SOC 2 Type II', type: 'Compliance', icon: '✅' }
]

onMounted(() => {
  if (process.client) {
    gsap.registerPlugin(ScrollTrigger)
    
    // Animate gradient text
    gsap.fromTo('.gradient-text',
      { backgroundPosition: '200% center' },
      {
        backgroundPosition: '-200% center',
        duration: 3,
        ease: 'none',
        repeat: -1
      }
    )
    
    // Animate award cards
    gsap.fromTo('.award-card',
      { opacity: 0, y: 50, scale: 0.9 },
      {
        opacity: 1,
        y: 0,
        scale: 1,
        duration: 0.8,
        stagger: 0.15,
        ease: 'back.out(1.7)',
        scrollTrigger: {
          trigger: '.award-card',
          start: 'top 85%',
          toggleActions: 'play none none reverse'
        }
      }
    )
    
    // Animate culture content
    gsap.fromTo('.culture-content',
      { opacity: 0, x: -50 },
      {
        opacity: 1,
        x: 0,
        duration: 1,
        ease: 'power3.out',
        scrollTrigger: {
          trigger: '.culture-content',
          start: 'top 80%',
          toggleActions: 'play none none reverse'
        }
      }
    )
    
    // Animate culture visual
    gsap.fromTo('.culture-visual',
      { opacity: 0, x: 50 },
      {
        opacity: 1,
        x: 0,
        duration: 1,
        ease: 'power3.out',
        scrollTrigger: {
          trigger: '.culture-visual',
          start: 'top 80%',
          toggleActions: 'play none none reverse'
        }
      }
    )
    
    // Animate counters
    const counters = document.querySelectorAll('.counter')
    counters.forEach(counter => {
      const target = parseInt(counter.dataset.target)
      gsap.fromTo(counter, 
        { innerHTML: 0 },
        {
          innerHTML: target,
          duration: 2,
          ease: 'power2.out',
          snap: { innerHTML: 1 },
          scrollTrigger: {
            trigger: counter,
            start: 'top 85%',
            toggleActions: 'play none none reverse'
          }
        }
      )
    })
  }
})
</script>

<style scoped>
.gradient-text {
  background: linear-gradient(270deg, #3b82f6, #10b981, #8b5cf6, #3b82f6);
  background-size: 400% 400%;
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  background-clip: text;
}
</style>