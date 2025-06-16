<template>
  <section class="section-padding bg-gradient-to-br from-gray-50 via-white to-gray-50 relative overflow-hidden">
    <!-- Background Pattern -->
    <div class="absolute inset-0 opacity-5">
      <div class="absolute inset-0" style="background-image: radial-gradient(circle at 25% 75%, rgba(59, 130, 246, 0.1) 0%, transparent 50%), radial-gradient(circle at 75% 25%, rgba(147, 51, 234, 0.1) 0%, transparent 50%);"></div>
    </div>

    <div class="container-custom relative z-10">
      <!-- Enhanced Header with Big Typography -->
      <div class="max-w-6xl mx-auto text-center mb-20">
        <div class="inline-flex items-center bg-purple-100 text-purple-800 px-6 py-3 rounded-full text-sm font-semibold mb-8 animate-pulse">
          <span class="w-2 h-2 bg-purple-500 rounded-full mr-3"></span>
          EXCELLENCE REDEFINED
        </div>
        
        <h2 class="text-6xl md:text-7xl lg:text-8xl font-bold mb-8 text-gray-900 font-heading leading-tight">
          Why Choose
          <span class="block gradient-text animate-gradient">Us</span>
        </h2>
        
        <p class="text-2xl md:text-3xl text-gray-600 leading-relaxed max-w-4xl mx-auto font-light">
          We drive <span class="font-semibold text-gray-800">exponential growth</span> through cutting-edge technologies and 
          scalable solutions that adapt to change, leveraging innovations to take your business 
          <span class="font-semibold gradient-text">beyond today's limits</span>.
        </p>
      </div>
      
      <!-- Interactive Features Grid -->
      <div class="grid lg:grid-cols-2 gap-8 mb-16">
        <div v-for="(feature, index) in features" :key="feature.title" 
             class="feature-card group relative bg-white p-10 rounded-3xl border border-gray-200 hover:border-purple-300 transition-all duration-500 cursor-pointer overflow-hidden"
             @mouseenter="handleFeatureHover(index, true)"
             @mouseleave="handleFeatureHover(index, false)">
          
          <!-- Card Background Animation -->
          <div class="absolute inset-0 bg-gradient-to-br from-purple-50 to-blue-50 opacity-0 group-hover:opacity-100 transition-opacity duration-500"></div>
          
          <!-- Content -->
          <div class="relative z-10 flex items-start space-x-6">
            <!-- Interactive Icon -->
            <div class="flex-shrink-0 relative">
              <div class="w-16 h-16 bg-gray-100 rounded-2xl flex items-center justify-center group-hover:bg-white group-hover:scale-110 transition-all duration-500 group-hover:shadow-lg">
                <component :is="feature.icon" class="w-8 h-8 text-gray-600 group-hover:text-purple-600 transition-all duration-500" />
              </div>
              <!-- Floating Badge -->
              <div class="absolute -top-2 -right-2 w-6 h-6 bg-purple-600 rounded-full opacity-0 group-hover:opacity-100 transition-all duration-500 flex items-center justify-center">
                <span class="text-white text-xs">✓</span>
              </div>
            </div>
            
            <div class="flex-1">
              <!-- Big Typography Title -->
              <h3 class="text-2xl md:text-3xl font-bold mb-4 text-gray-900 group-hover:text-purple-900 transition-colors duration-500 font-heading">
                {{ feature.title }}
              </h3>
              
              <!-- Enhanced Description -->
              <p class="text-gray-600 leading-relaxed mb-6 group-hover:text-gray-700 transition-colors duration-500">
                {{ feature.description }}
              </p>
              
              <!-- Interactive CTA -->
              <div class="flex items-center space-x-3 opacity-0 group-hover:opacity-100 transition-all duration-500 transform translate-y-4 group-hover:translate-y-0">
                <span class="text-purple-600 font-semibold text-sm">Learn More</span>
                <div class="w-6 h-6 bg-purple-600 rounded-full flex items-center justify-center">
                  <span class="text-white text-xs">→</span>
                </div>
              </div>
              
              <!-- Progress Bar -->
              <div class="mt-6 h-1 bg-gray-200 rounded-full overflow-hidden">
                <div class="feature-progress h-full bg-gradient-to-r from-purple-600 to-blue-600 rounded-full transform -translate-x-full group-hover:translate-x-0 transition-transform duration-1000"></div>
              </div>
            </div>
          </div>
        </div>
      </div>

      <!-- Interactive Value Proposition Section -->
      <div class="grid md:grid-cols-3 gap-8 mb-16">
        <div v-for="(value, index) in valueProps" :key="value.title"
             class="value-card group bg-white p-8 rounded-3xl border border-gray-200 hover:border-purple-300 transition-all duration-500 cursor-pointer text-center relative overflow-hidden"
             @mouseenter="handleValueHover(index, true)"
             @mouseleave="handleValueHover(index, false)">
          
          <!-- Card Background -->
          <div class="absolute inset-0 bg-gradient-to-br from-purple-50 to-blue-50 opacity-0 group-hover:opacity-100 transition-opacity duration-500"></div>
          
          <div class="relative z-10">
            <!-- Large Number -->
            <div class="text-5xl md:text-6xl font-bold text-gray-900 mb-4 group-hover:text-purple-600 transition-colors duration-500 counter" :data-target="value.number" :data-suffix="value.suffix">0</div>
            <h4 class="text-xl font-bold text-gray-900 mb-3 group-hover:text-purple-900 transition-colors duration-300">{{ value.title }}</h4>
            <p class="text-gray-600 group-hover:text-gray-700 transition-colors duration-300">{{ value.description }}</p>
            
          </div>
        </div>
      </div>

      <!-- Enhanced CTA Section -->
      <div class="bg-gray-900 rounded-3xl p-12 text-center text-white relative overflow-hidden">
        <!-- Background Animation -->
        <div class="absolute inset-0 bg-gradient-to-r from-purple-600/20 to-blue-600/20 animate-pulse"></div>
        
        <div class="relative z-10">
          <h3 class="text-4xl md:text-5xl font-bold mb-6 font-heading">
            Ready to Transform?
          </h3>
          <p class="text-xl text-gray-300 mb-8 max-w-2xl mx-auto">
            Join 500+ companies that have already revolutionized their business with our solutions.
          </p>
          
          <div class="flex flex-col sm:flex-row items-center justify-center gap-6">
            <button class="bg-white text-gray-900 px-8 py-4 rounded-full font-semibold hover:bg-gray-100 transition-all duration-300 transform hover:scale-105">
              Start Your Journey →
            </button>
            <button class="border-2 border-white text-white px-8 py-4 rounded-full font-semibold hover:bg-white hover:text-gray-900 transition-all duration-300">
              Schedule Consultation
            </button>
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
  UserGroupIcon,
  ArrowPathIcon,
  BoltIcon,
  RocketLaunchIcon,
  ShieldCheckIcon,
  ChartBarIcon
} from '@heroicons/vue/24/outline'

const features = [
  {
    icon: UserGroupIcon,
    title: 'Strategic Tech Partnership',
    description: 'We don\'t just deliver services – we become your tech partner, aligning our expertise with your goals to drive real impact.',
    progress: 0.95
  },
  {
    icon: ArrowPathIcon,
    title: 'Scalable Innovation',
    description: 'We harness emerging technologies to enable you to disrupt your industry and grow without limits.',
    progress: 0.88
  },
  {
    icon: BoltIcon,
    title: 'Optimized IT Efficiency',
    description: 'We focus on performance, reliability, and results ensuring your IT works smarter, faster, and better.',
    progress: 0.92
  },
  {
    icon: RocketLaunchIcon,
    title: 'Agile & Reliable Deployment',
    description: 'We ensure rapid, reliable deployments through an agile approach that minimizes downtime and safeguards business continuity.',
    progress: 0.90
  },
  {
    icon: ShieldCheckIcon,
    title: 'Proactive IT Continuity',
    description: 'We monitor your systems 24/7, solving issues before they arise and keeping your business running smoothly.',
    progress: 0.97
  },
  {
    icon: ChartBarIcon,
    title: 'Results-Driven Approach',
    description: 'Every solution is designed with measurable outcomes in mind, ensuring maximum ROI and business impact.',
    progress: 0.94
  }
]

const valueProps = [
  {
    number: 98,
    suffix: '%',
    title: 'Client Satisfaction',
    description: 'Consistently delivering exceptional results',
    progress: 0.98
  },
  {
    number: 300,
    suffix: '%',
    title: 'Average ROI',
    description: 'Measurable business impact',
    progress: 0.85
  },
  {
    number: 24,
    suffix: '/7',
    title: 'Support Available',
    description: 'Round-the-clock expert assistance',
    progress: 1.0
  }
]

const handleFeatureHover = (index, isHover) => {
  if (process.client) {
    const card = document.querySelectorAll('.feature-card')[index]
    if (isHover) {
      gsap.to(card, {
        y: -10,
        scale: 1.02,
        duration: 0.3,
        ease: 'power2.out'
      })
    } else {
      gsap.to(card, {
        y: 0,
        scale: 1,
        duration: 0.3,
        ease: 'power2.out'
      })
    }
  }
}

const handleValueHover = (index, isHover) => {
  if (process.client) {
    const card = document.querySelectorAll('.value-card')[index]
    if (isHover) {
      gsap.to(card, {
        y: -15,
        scale: 1.05,
        duration: 0.4,
        ease: 'power2.out'
      })
      
      // Animate counter
      const counter = card.querySelector('.counter')
      const target = parseInt(counter.dataset.target)
      const suffix = counter.dataset.suffix
      
      gsap.to(counter, {
        innerHTML: target,
        duration: 1.5,
        ease: 'power2.out',
        snap: { innerHTML: 1 },
        onUpdate: function() {
          counter.innerHTML = Math.ceil(counter.innerHTML) + suffix
        }
      })
    } else {
      gsap.to(card, {
        y: 0,
        scale: 1,
        duration: 0.4,
        ease: 'power2.out'
      })
      
      // Reset counter
      const counter = card.querySelector('.counter')
      gsap.to(counter, {
        innerHTML: 0,
        duration: 0.3
      })
    }
  }
}

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
    
    // Animate feature cards
    gsap.fromTo('.feature-card',
      { opacity: 0, y: 50, scale: 0.9 },
      {
        opacity: 1,
        y: 0,
        scale: 1,
        duration: 0.8,
        stagger: 0.15,
        ease: 'back.out(1.7)',
        scrollTrigger: {
          trigger: '.feature-card',
          start: 'top 85%',
          toggleActions: 'play none none reverse'
        }
      }
    )

    // Animate value cards
    gsap.fromTo('.value-card',
      { opacity: 0, y: 30 },
      {
        opacity: 1,
        y: 0,
        duration: 0.6,
        stagger: 0.1,
        ease: 'power3.out',
        scrollTrigger: {
          trigger: '.value-card',
          start: 'top 85%',
          toggleActions: 'play none none reverse'
        }
      }
    )
  }
})
</script>

<style scoped>
.animate-gradient {
  background: linear-gradient(270deg, #8b5cf6, #3b82f6, #8b5cf6);
  background-size: 400% 400%;
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  background-clip: text;
}

.feature-progress,
.progress-ring,
.value-ring {
  transition: all 1s cubic-bezier(0.4, 0, 0.2, 1);
}
</style>