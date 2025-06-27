<template>
  <section class="section-padding bg-white relative overflow-hidden">
    <!-- Background Pattern -->
    <div class="absolute inset-0 opacity-5">
      <div class="absolute inset-0" style="background-image: radial-gradient(circle at 20% 80%, rgba(59, 130, 246, 0.1) 0%, transparent 50%), radial-gradient(circle at 80% 20%, rgba(147, 51, 234, 0.1) 0%, transparent 50%);"></div>
    </div>

    <div class="container-custom relative z-10">
      <!-- Header -->
      <div class="max-w-4xl mx-auto text-center mb-20">
        <div class="inline-flex items-center bg-orange-100 text-orange-800 px-6 py-3 rounded-full text-sm font-semibold mb-8">
          <span class="w-2 h-2 bg-orange-500 rounded-full mr-3"></span>
          OUR CORE VALUES
        </div>
        
        <h2 class="text-5xl md:text-6xl lg:text-7xl font-bold mb-8 text-gray-900 font-heading leading-tight">
          Values That
          <span class="block gradient-text animate-gradient">Define</span>
          <span class="block text-4xl md:text-5xl lg:text-6xl text-gray-700">Our Culture</span>
        </h2>
        
        <p class="text-xl text-gray-600 leading-relaxed">
          These fundamental principles guide every decision we make and every solution we deliver, 
          ensuring we maintain the highest standards of excellence and integrity.
        </p>
      </div>

      <!-- Values Grid -->
      <div class="grid md:grid-cols-2 lg:grid-cols-3 gap-8 mb-16">
        <div v-for="(value, index) in values" :key="value.title"
             class="value-card group relative bg-white p-10 rounded-3xl border border-gray-200 hover:border-blue-300 transition-all duration-500 cursor-pointer overflow-hidden"
             @mouseenter="handleValueHover(index, true)"
             @mouseleave="handleValueHover(index, false)">
          
          <!-- Card Background Animation -->
          <div class="absolute inset-0 bg-gradient-to-br from-blue-50 to-purple-50 opacity-0 group-hover:opacity-100 transition-opacity duration-500"></div>
          
          <div class="relative z-10">
            <!-- Icon -->
            <div class="w-16 h-16 bg-gray-100 rounded-2xl flex items-center justify-center mb-8 group-hover:bg-white group-hover:scale-110 transition-all duration-500 group-hover:shadow-lg">
              <component :is="value.icon" class="w-8 h-8 text-gray-600 group-hover:text-blue-600 transition-all duration-500" />
            </div>
            
            <!-- Title -->
            <h3 class="text-2xl font-bold mb-4 text-gray-900 group-hover:text-blue-900 transition-colors duration-500 font-heading">
              {{ value.title }}
            </h3>
            
            <!-- Description -->
            <p class="text-gray-600 leading-relaxed mb-6 group-hover:text-gray-700 transition-colors duration-500">
              {{ value.description }}
            </p>
            
            <!-- Key Points -->
            <div class="space-y-3">
              <div v-for="point in value.points" :key="point" class="flex items-start space-x-3">
                <div class="w-1.5 h-1.5 bg-blue-600 rounded-full mt-2 flex-shrink-0"></div>
                <div class="text-sm text-gray-700">{{ point }}</div>
              </div>
            </div>
            
            <!-- Progress Bar -->
            <div class="mt-6 h-1 bg-gray-200 rounded-full overflow-hidden">
              <div class="value-progress h-full bg-gradient-to-r from-blue-600 to-purple-600 rounded-full transform -translate-x-full group-hover:translate-x-0 transition-transform duration-1000"></div>
            </div>
          </div>
        </div>
      </div>

      <!-- Culture Statement -->
      <div class="max-w-5xl mx-auto">
        <div class="bg-gradient-to-br from-gray-50 to-white p-12 rounded-3xl border border-gray-200 relative overflow-hidden">
          <div class="absolute inset-0 opacity-10">
            <div class="culture-float culture-float-1"></div>
            <div class="culture-float culture-float-2"></div>
            <div class="culture-float culture-float-3"></div>
          </div>
          
          <div class="relative z-10 text-center">
            <div class="w-20 h-20 bg-gray-900 rounded-2xl flex items-center justify-center mx-auto mb-8">
              <svg class="w-10 h-10 text-white" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4.318 6.318a4.5 4.5 0 000 6.364L12 20.364l7.682-7.682a4.5 4.5 0 00-6.364-6.364L12 7.636l-1.318-1.318a4.5 4.5 0 00-6.364 0z"></path>
              </svg>
            </div>
            
            <h3 class="text-3xl md:text-4xl font-bold mb-6 text-gray-900 font-heading">
              Building a Culture of Excellence
            </h3>
            
            <p class="text-lg text-gray-600 leading-relaxed mb-8 max-w-3xl mx-auto">
              Our values aren't just words on a wall – they're the foundation of how we work, 
              how we treat our clients, and how we continue to grow as a company. Every team member 
              embodies these principles in their daily work, creating an environment where 
              <span class="font-semibold text-gray-800">innovation thrives and excellence is the standard</span>.
            </p>
            
            <!-- Culture Stats -->
            <div class="grid grid-cols-2 md:grid-cols-4 gap-8">
              <div class="culture-stat">
                <div class="text-3xl font-bold text-blue-600 mb-2 counter" data-target="95">0</div>
                <div class="text-gray-600 text-sm">Employee Satisfaction</div>
              </div>
              <div class="culture-stat">
                <div class="text-3xl font-bold text-green-600 mb-2 counter" data-target="4.8">0</div>
                <div class="text-gray-600 text-sm">Team Rating</div>
              </div>
              <div class="culture-stat">
                <div class="text-3xl font-bold text-purple-600 mb-2 counter" data-target="92">0</div>
                <div class="text-gray-600 text-sm">Retention Rate</div>
              </div>
              <div class="culture-stat">
                <div class="text-3xl font-bold text-orange-600 mb-2 counter" data-target="15">0</div>
                <div class="text-gray-600 text-sm">Avg. Tenure (Years)</div>
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
  ShieldCheckIcon,
  LightBulbIcon,
  UsersIcon,
  TrophyIcon,
  HeartIcon,
  RocketLaunchIcon
} from '@heroicons/vue/24/outline'

const values = [
  {
    icon: ShieldCheckIcon,
    title: 'Integrity First',
    description: 'We build trust through transparent communication, ethical practices, and delivering on our promises every time.',
    points: [
      'Transparent project communication',
      'Ethical business practices',
      'Reliable delivery commitments'
    ]
  },
  {
    icon: LightBulbIcon,
    title: 'Innovation Drive',
    description: 'We constantly push the boundaries of what\'s possible, embracing new technologies to solve complex challenges.',
    points: [
      'Cutting-edge technology adoption',
      'Creative problem-solving approaches',
      'Continuous learning culture'
    ]
  },
  {
    icon: UsersIcon,
    title: 'Client Partnership',
    description: 'We view every client relationship as a long-term partnership, invested in their success and growth.',
    points: [
      'Strategic business alignment',
      'Proactive solution recommendations',
      'Long-term relationship focus'
    ]
  },
  {
    icon: TrophyIcon,
    title: 'Excellence Standard',
    description: 'We maintain the highest quality standards in everything we do, from code quality to customer service.',
    points: [
      'Rigorous quality assurance',
      'Best practice implementation',
      'Continuous improvement mindset'
    ]
  },
  {
    icon: HeartIcon,
    title: 'People Centered',
    description: 'We believe great technology comes from great people, fostering a culture of growth and collaboration.',
    points: [
      'Team development focus',
      'Collaborative work environment',
      'Work-life balance priority'
    ]
  },
  {
    icon: RocketLaunchIcon,
    title: 'Impact Focused',
    description: 'Every solution we create is designed to deliver measurable business impact and drive real results.',
    points: [
      'ROI-driven solutions',
      'Measurable outcome tracking',
      'Business value optimization'
    ]
  }
]

const handleValueHover = (index, isHover) => {
  if (process.client) {
    const card = document.querySelectorAll('.value-card')[index]
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
    
    // Animate value cards
    gsap.fromTo('.value-card',
      { opacity: 0, y: 50, scale: 0.9 },
      {
        opacity: 1,
        y: 0,
        scale: 1,
        duration: 0.8,
        stagger: 0.15,
        ease: 'back.out(1.7)',
        scrollTrigger: {
          trigger: '.value-card',
          start: 'top 85%',
          toggleActions: 'play none none reverse'
        }
      }
    )
    
    // Animate culture stats
    gsap.fromTo('.culture-stat',
      { opacity: 0, y: 30 },
      {
        opacity: 1,
        y: 0,
        duration: 0.6,
        stagger: 0.1,
        ease: 'back.out(1.7)',
        scrollTrigger: {
          trigger: '.culture-stat',
          start: 'top 85%',
          toggleActions: 'play none none reverse'
        }
      }
    )
    
    // Animate counters
    const counters = document.querySelectorAll('.counter')
    counters.forEach(counter => {
      const target = parseFloat(counter.dataset.target)
      gsap.fromTo(counter, 
        { innerHTML: 0 },
        {
          innerHTML: target,
          duration: 2,
          ease: 'power2.out',
          snap: { innerHTML: target < 10 ? 0.1 : 1 },
          scrollTrigger: {
            trigger: counter,
            start: 'top 85%',
            toggleActions: 'play none none reverse'
          }
        }
      )
    })
    
    // Floating culture elements
    gsap.to('.culture-float-1', { y: -15, duration: 3, yoyo: true, repeat: -1, ease: 'sine.inOut' })
    gsap.to('.culture-float-2', { y: -20, duration: 4, yoyo: true, repeat: -1, ease: 'sine.inOut', delay: 1 })
    gsap.to('.culture-float-3', { y: -25, duration: 3.5, yoyo: true, repeat: -1, ease: 'sine.inOut', delay: 2 })
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

.culture-float {
  position: absolute;
  width: 8px;
  height: 8px;
  background: linear-gradient(45deg, #3b82f6, #10b981);
  border-radius: 50%;
  opacity: 0.6;
}

.culture-float-1 { top: 10%; left: 10%; }
.culture-float-2 { top: 70%; right: 15%; }
.culture-float-3 { bottom: 20%; left: 20%; }
</style>