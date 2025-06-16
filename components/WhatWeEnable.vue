<template>
  <section class="section-padding bg-gradient-to-br from-gray-50 to-white relative overflow-hidden">
    <!-- Background Pattern -->
    <div class="absolute inset-0 opacity-5">
      <div class="absolute inset-0" style="background-image: radial-gradient(circle at 20% 80%, rgba(59, 130, 246, 0.1) 0%, transparent 50%), radial-gradient(circle at 80% 20%, rgba(147, 51, 234, 0.1) 0%, transparent 50%);"></div>
    </div>

    <div class="container-custom relative z-10">
      <!-- Enhanced Header with Big Typography -->
      <div class="max-w-6xl mx-auto text-center mb-20">
        <div class="inline-flex items-center bg-blue-100 text-blue-800 px-6 py-3 rounded-full text-sm font-semibold mb-8 animate-pulse">
          <span class="w-2 h-2 bg-blue-500 rounded-full mr-3"></span>
          INNOVATION UNLEASHED
        </div>
        
        <h2 class="text-6xl md:text-7xl lg:text-8xl font-bold mb-8 text-gray-900 font-heading leading-tight">
          What We
          <span class="block gradient-text animate-gradient">Enable</span>
        </h2>
        
        <p class="text-2xl md:text-3xl text-gray-600 leading-relaxed max-w-4xl mx-auto font-light">
          The future, <span class="font-semibold text-gray-800">engineered</span>. 
          We architect the technologies that redefine boundaries, 
          empower innovation, and unlock the next era of 
          <span class="font-semibold gradient-text">digital transformation</span>.
        </p>
      </div>
      
      <!-- Interactive Services Grid -->
      <div class="grid md:grid-cols-2 lg:grid-cols-3 gap-8 mb-16">
        <div v-for="(service, index) in services" :key="service.title" 
             class="service-card group relative bg-white p-8 rounded-3xl border border-gray-200 hover:border-blue-300 transition-all duration-500 cursor-pointer overflow-hidden"
             @mouseenter="handleCardHover(index, true)"
             @mouseleave="handleCardHover(index, false)">
          
          <!-- Card Background Animation -->
          <div class="absolute inset-0 bg-gradient-to-br from-blue-50 to-purple-50 opacity-0 group-hover:opacity-100 transition-opacity duration-500"></div>
          
          <!-- Content -->
          <div class="relative z-10">
            <!-- Interactive Icon -->
            <div class="relative mb-8">
              <div class="w-16 h-16 bg-gray-100 rounded-2xl flex items-center justify-center group-hover:bg-white group-hover:scale-110 transition-all duration-500 group-hover:shadow-lg">
                <component :is="service.icon" class="w-8 h-8 text-gray-600 group-hover:text-blue-600 transition-all duration-500" />
              </div>
              <!-- Floating Badge -->
              <div class="absolute -top-2 -right-2 w-6 h-6 bg-blue-600 rounded-full opacity-0 group-hover:opacity-100 transition-all duration-500 flex items-center justify-center">
                <span class="text-white text-xs">→</span>
              </div>
            </div>
            
            <!-- Big Typography Title -->
            <h3 class="text-2xl md:text-3xl font-bold mb-6 text-gray-900 group-hover:text-blue-900 transition-colors duration-500 font-heading">
              {{ service.title }}
            </h3>
            
            <!-- Enhanced Description -->
            <p class="text-gray-600 leading-relaxed mb-6 group-hover:text-gray-700 transition-colors duration-500">
              {{ service.description }}
            </p>
            
            <!-- Interactive CTA -->
            <div class="flex items-center space-x-3 opacity-0 group-hover:opacity-100 transition-all duration-500 transform translate-y-4 group-hover:translate-y-0">
              <span class="text-blue-600 font-semibold text-sm">Explore Solution</span>
              <div class="w-6 h-6 bg-blue-600 rounded-full flex items-center justify-center">
                <span class="text-white text-xs">→</span>
              </div>
            </div>
            
            <!-- Progress Bar -->
            <div class="mt-6 h-1 bg-gray-200 rounded-full overflow-hidden">
              <div class="progress-bar h-full bg-gradient-to-r from-blue-600 to-purple-600 rounded-full transform -translate-x-full group-hover:translate-x-0 transition-transform duration-1000"></div>
            </div>
          </div>
        </div>
      </div>

      <!-- Interactive Stats Section -->
      <div class="bg-gray-900 rounded-3xl p-12 text-center text-white relative overflow-hidden">
        <!-- Background Animation -->
        <div class="absolute inset-0 bg-gradient-to-r from-blue-600/20 to-purple-600/20 animate-pulse"></div>
        
        <div class="relative z-10">
          <h3 class="text-4xl md:text-5xl font-semibold mb-8 font-heading">
            Transforming Industries
          </h3>
          
          <div class="grid grid-cols-2 md:grid-cols-4 gap-8">
            <div v-for="(stat, index) in stats" :key="stat.label" class="stat-item cursor-pointer">
              <div class="text-4xl md:text-5xl font-semibold mb-2 counter" :data-target="stat.value">0</div>
              <div class="text-gray-300 text-sm">{{ stat.label }}</div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
import { onMounted, ref } from 'vue'
import { gsap } from 'gsap'
import { ScrollTrigger } from 'gsap/ScrollTrigger'
import { 
  RocketLaunchIcon,
  ShieldCheckIcon,
  CloudIcon,
  CpuChipIcon,
  DevicePhoneMobileIcon,
  BoltIcon
} from '@heroicons/vue/24/outline'

const services = [
  {
    icon: RocketLaunchIcon,
    title: 'Digital Innovation',
    description: 'Transform your business with cutting-edge digital solutions that drive exponential growth and operational efficiency.'
  },
  {
    icon: ShieldCheckIcon,
    title: 'Cybersecurity',
    description: 'Protect your digital assets with enterprise-grade security solutions, monitoring, and threat intelligence.'
  },
  {
    icon: CloudIcon,
    title: 'Cloud Solutions',
    description: 'Migrate and optimize your infrastructure with scalable, secure cloud technologies and architectures.'
  },
  {
    icon: CpuChipIcon,
    title: 'AI & Machine Learning',
    description: 'Harness artificial intelligence to automate processes, predict outcomes, and optimize operations.'
  },
  {
    icon: DevicePhoneMobileIcon,
    title: 'Mobile Development',
    description: 'Create powerful, intuitive mobile applications that engage users and drive measurable business value.'
  },
  {
    icon: BoltIcon,
    title: 'Performance Optimization',
    description: 'Enhance system performance, reliability, and scalability with advanced optimization techniques.'
  }
]

const stats = [
  { value: 500, label: 'Projects Delivered' },
  { value: 150, label: 'Enterprise Clients' },
  { value: 25, label: 'Countries Served' },
  { value: 98, label: 'Success Rate' }
]

const handleCardHover = (index, isHover) => {
  if (process.client) {
    const card = document.querySelectorAll('.service-card')[index]
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
    
    // Animate title
    gsap.fromTo('.gradient-text',
      { backgroundPosition: '200% center' },
      {
        backgroundPosition: '-200% center',
        duration: 3,
        ease: 'none',
        repeat: -1
      }
    )
    
    // Animate service cards
    gsap.fromTo('.service-card',
      { opacity: 0, y: 50, scale: 0.9 },
      {
        opacity: 1,
        y: 0,
        scale: 1,
        duration: 0.8,
        stagger: 0.15,
        ease: 'back.out(1.7)',
        scrollTrigger: {
          trigger: '.service-card',
          start: 'top 85%',
          toggleActions: 'play none none reverse'
        }
      }
    )

    // Animate counters
    const animateCounters = () => {
      const counters = document.querySelectorAll('.counter')
      counters.forEach((counter, index) => {
        const target = parseInt(counter.dataset.target)
        gsap.to(counter, {
          innerHTML: target,
          duration: 2,
          delay: index * 0.2,
          ease: 'power2.out',
          snap: { innerHTML: 1 },
          onUpdate: function() {
            const suffix = index === 3 ? '%' : '+'
            counter.innerHTML = Math.ceil(counter.innerHTML) + suffix
          }
        })
      })
    }

    ScrollTrigger.create({
      trigger: '.stat-item',
      start: 'top 80%',
      onEnter: animateCounters,
      once: true
    })

    // Add hover effects to stats
    const statItems = document.querySelectorAll('.stat-item')
    statItems.forEach(item => {
      item.addEventListener('mouseenter', () => {
        gsap.to(item, {
          scale: 1.1,
          duration: 0.3,
          ease: 'power2.out'
        })
      })
      
      item.addEventListener('mouseleave', () => {
        gsap.to(item, {
          scale: 1,
          duration: 0.3,
          ease: 'power2.out'
        })
      })
    })
  }
})
</script>

<style scoped>
.animate-gradient {
  background: linear-gradient(270deg, #3b82f6, #8b5cf6, #3b82f6);
  background-size: 400% 400%;
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  background-clip: text;
}

.progress-bar {
  transition: transform 1s cubic-bezier(0.4, 0, 0.2, 1);
}
</style>