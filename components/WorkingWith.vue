<template>
  <section class="section-padding bg-gray-900 relative overflow-hidden">
    <!-- Background Pattern -->
    <div class="absolute inset-0 opacity-10">
      <div class="absolute inset-0" style="background-image: radial-gradient(circle at 15% 85%, rgba(59, 130, 246, 0.2) 0%, transparent 50%), radial-gradient(circle at 85% 15%, rgba(147, 51, 234, 0.2) 0%, transparent 50%);"></div>
    </div>

    <!-- Animated Background Dots -->
    <div class="absolute inset-0 opacity-20">
      <div class="floating-dots">
        <div class="dot dot-1"></div>
        <div class="dot dot-2"></div>
        <div class="dot dot-3"></div>
        <div class="dot dot-4"></div>
        <div class="dot dot-5"></div>
      </div>
    </div>

    <div class="container-custom relative z-10">
      <!-- Enhanced Header with Big Typography -->
      <div class="max-w-6xl mx-auto text-center mb-20">
        <div class="inline-flex items-center bg-blue-900/30 text-blue-300 px-6 py-3 rounded-full text-sm font-semibold mb-8 animate-pulse border border-blue-800">
          <span class="w-2 h-2 bg-blue-400 rounded-full mr-3"></span>
          TECHNOLOGY MASTERY
        </div>
        
        <h2 class="text-6xl md:text-7xl lg:text-8xl font-bold mb-8 text-white font-heading leading-tight">
          Working
          <span class="block gradient-text-dark animate-gradient">With</span>
          <span class="block text-5xl md:text-6xl lg:text-7xl text-gray-300">Leading Technologies</span>
        </h2>
        
        <p class="text-2xl md:text-3xl text-gray-300 leading-relaxed max-w-4xl mx-auto font-light">
          Drive <span class="font-semibold text-white">digital transformation</span> across your organization 
          with our specialized knowledge of key software and platforms that power 
          <span class="font-semibold gradient-text-dark">modern enterprises</span>.
        </p>
      </div>

      <!-- Interactive Technology Categories -->
      <div class="grid md:grid-cols-2 lg:grid-cols-3 gap-8 mb-20">
        <div v-for="(category, index) in techCategories" :key="category.title"
             class="tech-category group relative bg-gray-800/50 backdrop-blur-sm p-8 rounded-3xl border border-gray-700 hover:border-blue-500 transition-all duration-500 cursor-pointer overflow-hidden"
             @mouseenter="handleCategoryHover(index, true)"
             @mouseleave="handleCategoryHover(index, false)">
          
          <!-- Card Background Animation -->
          <div class="absolute inset-0 bg-gradient-to-br from-blue-900/20 to-purple-900/20 opacity-0 group-hover:opacity-100 transition-opacity duration-500"></div>
          
          <div class="relative z-10">
            <!-- Category Icon -->
            <div class="w-16 h-16 bg-gray-700 rounded-2xl flex items-center justify-center mb-6 group-hover:bg-gray-600 group-hover:scale-110 transition-all duration-500 group-hover:shadow-lg">
              <component :is="category.icon" class="w-8 h-8 text-gray-400 group-hover:text-blue-400 transition-all duration-500" />
            </div>
            
            <!-- Category Title -->
            <h3 class="text-2xl font-bold mb-4 text-white group-hover:text-blue-200 transition-colors duration-500 font-heading">
              {{ category.title }}
            </h3>
            
            <!-- Technology Count -->
            <div class="text-gray-400 mb-6 group-hover:text-gray-300 transition-colors duration-300">
              {{ category.count }}+ Technologies
            </div>
            
            <!-- Technology Pills -->
            <div class="flex flex-wrap gap-2 mb-6">
              <span v-for="tech in category.technologies" :key="tech"
                    class="px-3 py-1 bg-gray-700 text-gray-300 text-xs rounded-full group-hover:bg-gray-600 group-hover:text-white transition-all duration-300">
                {{ tech }}
              </span>
            </div>
            
            <!-- Progress Bar -->
            <div class="h-1 bg-gray-700 rounded-full overflow-hidden">
              <div class="category-progress h-full bg-gradient-to-r from-blue-500 to-purple-500 rounded-full transform -translate-x-full group-hover:translate-x-0 transition-transform duration-1000"></div>
            </div>
          </div>
        </div>
      </div>
      
      <!-- Enhanced Platforms Grid -->
      <div class="platforms-section mb-16">
        <div class="text-center mb-12">
          <h3 class="text-4xl md:text-5xl font-bold mb-4 text-white font-heading">
            Our Technology Stack
          </h3>
          <p class="text-xl text-gray-400">
            Expertise across the entire technology ecosystem
          </p>
        </div>
        
        <div class="grid grid-cols-3 md:grid-cols-4 lg:grid-cols-6 gap-6">
          <div v-for="(platform, index) in platforms" :key="platform.name" 
               class="platform-item group relative bg-gray-800/50 backdrop-blur-sm p-6 rounded-2xl text-center border border-gray-700 hover:border-blue-500 transition-all duration-500 cursor-pointer overflow-hidden"
               @mouseenter="handlePlatformHover(index, true)"
               @mouseleave="handlePlatformHover(index, false)">
            
            <!-- Hover Background -->
            <div class="absolute inset-0 bg-gradient-to-br from-blue-900/30 to-purple-900/30 opacity-0 group-hover:opacity-100 transition-opacity duration-500"></div>
            
            <div class="relative z-10">
              <!-- Platform Icon -->
              <div class="w-12 h-12 mx-auto mb-4 flex items-center justify-center rounded-xl bg-gray-700 group-hover:bg-gray-600 group-hover:scale-110 transition-all duration-500">
                <component :is="platform.icon" class="w-6 h-6 text-gray-400 group-hover:text-blue-400 transition-all duration-500" />
              </div>
              
              <!-- Platform Name -->
              <span class="text-sm font-medium text-gray-300 group-hover:text-white transition-colors duration-300">
                {{ platform.name }}
              </span>
              
              <!-- Expertise Level -->
              <div class="w-full bg-gray-700 rounded-full h-1.5 mt-3 opacity-0 group-hover:opacity-100 transition-opacity duration-500">
                <div class="bg-gradient-to-r from-blue-500 to-purple-500 h-1.5 rounded-full transition-all duration-1000" 
                     :style="`width: ${platform.expertise}%`"></div>
              </div>
            </div>
            
            
          </div>
        </div>
      </div>

      <!-- Enhanced CTA Section -->
      <div class="bg-gradient-to-r from-blue-900 to-purple-900 rounded-3xl p-12 text-center text-white relative overflow-hidden">
        <div class="absolute inset-0 bg-gradient-to-r from-blue-600/20 to-purple-600/20 animate-pulse"></div>
        
        <div class="relative z-10">
          <h3 class="text-4xl md:text-5xl font-bold mb-6 font-heading">
            Ready to Innovate?
          </h3>
          <p class="text-xl text-blue-100 mb-8 max-w-2xl mx-auto">
            Let's discuss how our technology expertise can accelerate your digital transformation.
          </p>
          
          <div class="flex flex-col sm:flex-row items-center justify-center gap-6">
            <button class="bg-white text-gray-900 px-8 py-4 rounded-full font-semibold hover:bg-gray-100 transition-all duration-300 transform hover:scale-105">
              Discuss Your Project →
            </button>
            <button class="border-2 border-white text-white px-8 py-4 rounded-full font-semibold hover:bg-white hover:text-gray-900 transition-all duration-300">
              View Our Portfolio
            </button>
          </div>

          <!-- Tech Stats -->
          <div class="grid grid-cols-3 gap-8 mt-12 max-w-2xl mx-auto">
            <div class="text-center">
              <div class="text-3xl font-bold text-white mb-2">50+</div>
              <div class="text-sm text-blue-200">Technologies</div>
            </div>
            <div class="text-center">
              <div class="text-3xl font-bold text-white mb-2">15+</div>
              <div class="text-sm text-blue-200">Years Experience</div>
            </div>
            <div class="text-center">
              <div class="text-3xl font-bold text-white mb-2">100%</div>
              <div class="text-sm text-blue-200">Up to Date</div>
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

const techCategories = [
  {
    title: 'Cloud Platforms',
    icon: CloudIcon,
    count: 8,
    technologies: ['AWS', 'Azure', 'GCP', 'Docker'],
    progress: 0.95
  },
  {
    title: 'Development',
    icon: CodeBracketIcon,
    count: 12,
    technologies: ['React', 'Node.js', 'Python', 'C#'],
    progress: 0.90
  },
  {
    title: 'Databases',
    icon: CircleStackIcon,
    count: 6,
    technologies: ['SQL', 'MongoDB', 'Redis', 'Oracle'],
    progress: 0.88
  }
]

const platforms = [
  { name: 'Microsoft', icon: WindowIcon, expertise: 95 },
  { name: 'C#', icon: CodeBracketIcon, expertise: 90 },
  { name: 'Kotlin', icon: CubeIcon, expertise: 85 },
  { name: 'Android', icon: DevicePhoneMobileIcon, expertise: 88 },
  { name: 'SQL', icon: CircleStackIcon, expertise: 92 },
  { name: 'JavaScript', icon: CommandLineIcon, expertise: 94 },
  { name: 'AWS', icon: CloudIcon, expertise: 96 },
  { name: 'Azure', icon: ServerIcon, expertise: 89 },
  { name: 'Docker', icon: CubeIcon, expertise: 87 },
  { name: 'React', icon: AtSymbolIcon, expertise: 93 },
  { name: 'Node.js', icon: ServerIcon, expertise: 91 },
  { name: 'Python', icon: RocketLaunchIcon, expertise: 88 }
]

const handleCategoryHover = (index, isHover) => {
  if (process.client) {
    const card = document.querySelectorAll('.tech-category')[index]
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

const handlePlatformHover = (index, isHover) => {
  if (process.client) {
    const card = document.querySelectorAll('.platform-item')[index]
    if (isHover) {
      gsap.to(card, {
        y: -8,
        scale: 1.05,
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
    gsap.fromTo('.gradient-text-dark',
      { backgroundPosition: '200% center' },
      {
        backgroundPosition: '-200% center',
        duration: 4,
        ease: 'none',
        repeat: -1
      }
    )
    
    // Animate tech categories
    gsap.fromTo('.tech-category',
      { opacity: 0, y: 50, scale: 0.9 },
      {
        opacity: 1,
        y: 0,
        scale: 1,
        duration: 0.8,
        stagger: 0.15,
        ease: 'back.out(1.7)',
        scrollTrigger: {
          trigger: '.tech-category',
          start: 'top 85%',
          toggleActions: 'play none none reverse'
        }
      }
    )
    
    // Animate platform items
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

    // Animate floating dots
    gsap.to('.dot-1', { y: -20, duration: 2, yoyo: true, repeat: -1, ease: 'sine.inOut' })
    gsap.to('.dot-2', { y: -30, duration: 2.5, yoyo: true, repeat: -1, ease: 'sine.inOut', delay: 0.5 })
    gsap.to('.dot-3', { y: -25, duration: 3, yoyo: true, repeat: -1, ease: 'sine.inOut', delay: 1 })
    gsap.to('.dot-4', { y: -35, duration: 2.2, yoyo: true, repeat: -1, ease: 'sine.inOut', delay: 1.5 })
    gsap.to('.dot-5', { y: -15, duration: 2.8, yoyo: true, repeat: -1, ease: 'sine.inOut', delay: 2 })
  }
})
</script>

<style scoped>
.gradient-text-dark {
  background: linear-gradient(270deg, #60a5fa, #a78bfa, #34d399, #60a5fa);
  background-size: 400% 400%;
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  background-clip: text;
}

.category-progress {
  transition: transform 1s cubic-bezier(0.4, 0, 0.2, 1);
}

.floating-dots {
  position: absolute;
  inset: 0;
  pointer-events: none;
}

.dot {
  position: absolute;
  width: 8px;
  height: 8px;
  background: linear-gradient(45deg, #3b82f6, #8b5cf6);
  border-radius: 50%;
  opacity: 0.6;
}

.dot-1 { top: 20%; left: 10%; }
.dot-2 { top: 40%; right: 15%; }
.dot-3 { bottom: 30%; left: 20%; }
.dot-4 { top: 60%; left: 50%; }
.dot-5 { bottom: 20%; right: 25%; }
</style>