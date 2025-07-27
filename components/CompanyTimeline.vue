<template>
  <section class="section-padding bg-white relative overflow-hidden">
    <!-- Background Pattern -->
    <div class="absolute inset-0 opacity-5">
      <div class="absolute inset-0" style="background-image: radial-gradient(circle at 20% 80%, rgba(59, 130, 246, 0.1) 0%, transparent 50%), radial-gradient(circle at 80% 20%, rgba(147, 51, 234, 0.1) 0%, transparent 50%);"></div>
    </div>

    <div class="container-custom relative z-10">
      <!-- Header -->
      <div class="max-w-4xl mx-auto text-center mb-20">
        <div class="inline-flex items-center bg-green-100 text-green-800 px-6 py-3 rounded-full text-sm font-semibold mb-8">
          <span class="w-2 h-2 bg-green-500 rounded-full mr-3"></span>
          COMPANY TIMELINE
        </div>
        
        <h2 class="text-5xl md:text-6xl lg:text-7xl font-bold mb-8 text-gray-900 font-heading leading-tight">
          Our Journey
          <span class="block gradient-text animate-gradient">Through</span>
          <span class="block text-4xl md:text-5xl lg:text-6xl text-gray-700">Innovation</span>
        </h2>
        
        <p class="text-xl text-gray-600 leading-relaxed">
          From humble beginnings to industry leadership - here's how we've evolved 
          to become a trusted partner for enterprise digital transformation.
        </p>
      </div>

      <!-- Timeline -->
      <div class="max-w-4xl mx-auto">
        <div class="relative">
          <!-- Timeline Line -->
          <div class="absolute left-8 md:left-1/2 top-0 bottom-0 w-0.5 bg-gray-200 transform md:-translate-x-px"></div>
          
          <div class="space-y-12">
            <div v-for="(milestone, index) in timeline" :key="milestone.year"
                 :class="[
                   'timeline-item relative flex items-start',
                   index % 2 === 0 ? 'md:flex-row' : 'md:flex-row-reverse'
                 ]">
              
              <!-- Timeline Dot -->
              <div class="absolute left-8 md:left-1/2 w-4 h-4 bg-blue-600 rounded-full transform -translate-x-2 md:-translate-x-2 border-4 border-white shadow-lg z-10"></div>
              
              <!-- Content -->
              <div :class="[
                'ml-20 md:ml-0 md:w-1/2',
                index % 2 === 0 ? 'md:pr-12' : 'md:pl-12'
              ]">
                <div class="bg-white p-8 rounded-3xl border border-gray-200 hover:border-blue-300 transition-all duration-500 cursor-pointer group">
                  <div class="absolute inset-0 bg-gradient-to-br from-blue-50 to-purple-50 opacity-0 group-hover:opacity-100 transition-opacity duration-500 rounded-3xl"></div>
                  
                  <div class="relative z-10">
                    <div class="flex items-center space-x-4 mb-4">
                      <div class="w-12 h-12 bg-blue-100 rounded-xl flex items-center justify-center group-hover:bg-blue-200 transition-colors duration-300">
                        <component :is="milestone.icon" class="w-6 h-6 text-blue-600" />
                      </div>
                      <div>
                        <div class="text-2xl font-bold text-blue-600">{{ milestone.year }}</div>
                        <div class="text-sm text-gray-500">{{ milestone.quarter }}</div>
                      </div>
                    </div>
                    
                    <h3 class="text-xl font-bold mb-3 text-gray-900 group-hover:text-blue-900 transition-colors duration-300">
                      {{ milestone.title }}
                    </h3>
                    
                    <p class="text-gray-600 leading-relaxed mb-4 group-hover:text-gray-700 transition-colors duration-300">
                      {{ milestone.description }}
                    </p>
                    
                    <!-- Achievement Stats -->
                    <div class="grid grid-cols-2 gap-4 mt-6">
                      <div v-for="stat in milestone.stats" :key="stat.label" class="text-center p-3 bg-gray-50 rounded-xl group-hover:bg-white transition-colors duration-300">
                        <div class="text-lg font-bold text-blue-600">{{ stat.value }}</div>
                        <div class="text-xs text-gray-500">{{ stat.label }}</div>
                      </div>
                    </div>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>

      <!-- Future Vision -->
      <div class="max-w-4xl mx-auto mt-20">
        <div class="bg-gray-900 rounded-3xl p-12 text-white relative overflow-hidden">
          <div class="absolute inset-0 bg-gradient-to-r from-blue-600/20 to-purple-600/20 animate-pulse"></div>
          
          <div class="relative z-10 text-center">
            <div class="w-16 h-16 bg-lime-400 rounded-2xl flex items-center justify-center mx-auto mb-6">
              <svg class="w-8 h-8 text-gray-900" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M13 10V3L4 14h7v7l9-11h-7z"></path>
              </svg>
            </div>
            
            <h3 class="text-3xl md:text-4xl font-bold mb-6 font-heading">
              Looking Ahead to 2030
            </h3>
            
            <p class="text-xl text-gray-300 mb-8 max-w-3xl mx-auto">
              Our vision for the next chapter: empowering 10,000+ enterprises globally with 
              cutting-edge AI solutions and becoming the definitive leader in digital transformation.
            </p>
            
            <div class="grid grid-cols-2 md:grid-cols-4 gap-8">
              <div class="future-goal">
                <div class="text-3xl font-bold text-lime-400 mb-2">10K+</div>
                <div class="text-gray-300 text-sm">Global Enterprises</div>
              </div>
              <div class="future-goal">
                <div class="text-3xl font-bold text-blue-400 mb-2">50+</div>
                <div class="text-gray-300 text-sm">Countries</div>
              </div>
              <div class="future-goal">
                <div class="text-3xl font-bold text-purple-400 mb-2">$10B+</div>
                <div class="text-gray-300 text-sm">Value Generated</div>
              </div>
              <div class="future-goal">
                <div class="text-3xl font-bold text-green-400 mb-2">100%</div>
                <div class="text-gray-300 text-sm">Carbon Neutral</div>
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
  RocketLaunchIcon,
  GlobeAltIcon,
  TrophyIcon,
  UserGroupIcon,
  CpuChipIcon,
  ShieldCheckIcon,
  BoltIcon,
  StarIcon
} from '@heroicons/vue/24/outline'

const timeline = [
  {
    year: '2009',
    quarter: 'Q3',
    icon: RocketLaunchIcon,
    title: 'Company Founded',
    description: 'Michael Brown and Sarah Chen founded The qexle with a vision to bridge the gap between cutting-edge technology and business transformation.',
    stats: [
      { value: '3', label: 'Founding Team' },
      { value: '$50K', label: 'Initial Investment' }
    ]
  },
  {
    year: '2012',
    quarter: 'Q1',
    icon: UserGroupIcon,
    title: 'First Enterprise Client',
    description: 'Secured our first Fortune 500 client and delivered a transformational cloud migration project that saved them $2M annually.',
    stats: [
      { value: '15', label: 'Team Members' },
      { value: '$2M', label: 'Client Savings' }
    ]
  },
  {
    year: '2015',
    quarter: 'Q2',
    icon: GlobeAltIcon,
    title: 'Global Expansion',
    description: 'Opened offices in 5 countries and established strategic partnerships with major cloud providers including AWS and Microsoft.',
    stats: [
      { value: '5', label: 'Countries' },
      { value: '50+', label: 'Employees' }
    ]
  },
  {
    year: '2018',
    quarter: 'Q4',
    icon: TrophyIcon,
    title: 'Industry Recognition',
    description: 'Named "Digital Transformation Company of the Year" and achieved 98% client satisfaction rate across all projects.',
    stats: [
      { value: '98%', label: 'Satisfaction' },
      { value: '100+', label: 'Projects' }
    ]
  },
  {
    year: '2020',
    quarter: 'Q1',
    icon: CpuChipIcon,
    title: 'AI Leadership',
    description: 'Launched AI-first transformation services and became recognized leader in enterprise AI implementation and machine learning solutions.',
    stats: [
      { value: '50+', label: 'AI Projects' },
      { value: '150+', label: 'Team Size' }
    ]
  },
  {
    year: '2022',
    quarter: 'Q3',
    icon: ShieldCheckIcon,
    title: 'Security Excellence',
    description: 'Achieved ISO 27001 certification and launched comprehensive cybersecurity practice, maintaining zero security breaches record.',
    stats: [
      { value: '0', label: 'Breaches' },
      { value: '99.9%', label: 'Uptime' }
    ]
  },
  {
    year: '2024',
    quarter: 'Q2',
    icon: BoltIcon,
    title: 'Innovation Hub',
    description: 'Opened dedicated R&D innovation center and launched next-generation enterprise automation platform powered by advanced AI.',
    stats: [
      { value: '$2.3B+', label: 'Value Generated' },
      { value: '300+', label: 'Enterprises' }
    ]
  },
  {
    year: '2025',
    quarter: 'Q1',
    icon: StarIcon,
    title: 'Industry Pioneer',
    description: 'Recognized as the definitive leader in enterprise digital transformation, trusted by Fortune 500 companies worldwide.',
    stats: [
      { value: '500+', label: 'Projects' },
      { value: '25', label: 'Countries' }
    ]
  }
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
    
    // Animate timeline items
    gsap.fromTo('.timeline-item',
      { opacity: 0, y: 50 },
      {
        opacity: 1,
        y: 0,
        duration: 0.8,
        stagger: 0.2,
        ease: 'power3.out',
        scrollTrigger: {
          trigger: '.timeline-item',
          start: 'top 85%',
          toggleActions: 'play none none reverse'
        }
      }
    )
    
    // Animate future goals
    gsap.fromTo('.future-goal',
      { opacity: 0, y: 30 },
      {
        opacity: 1,
        y: 0,
        duration: 0.6,
        stagger: 0.1,
        ease: 'back.out(1.7)',
        scrollTrigger: {
          trigger: '.future-goal',
          start: 'top 85%',
          toggleActions: 'play none none reverse'
        }
      }
    )
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