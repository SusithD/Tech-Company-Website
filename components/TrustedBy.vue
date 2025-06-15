<template>
  <section class="py-16 bg-white border-b border-gray-100">
    <div class="container-custom">
      <div class="text-center mb-12">
        <p class="text-gray-500 font-medium mb-8">Trusted by 500+ global companies</p>
      </div>
      
      <!-- Interactive Logo Slider -->
      <div class="relative overflow-hidden">
        <div 
          ref="logoSlider"
          class="flex items-center space-x-12 animate-slide"
          style="animation-duration: 30s;"
        >
          <!-- First set of logos -->
          <div v-for="company in [...companies, ...companies]" :key="`${company.name}-${Math.random()}`" 
               class="company-logo flex-shrink-0 flex items-center justify-center h-16 w-32 transition-all duration-300 hover:scale-110 cursor-pointer group">
            <div class="flex items-center space-x-3">
              <component 
                :is="company.icon" 
                class="w-8 h-8 text-gray-400 group-hover:text-gray-700 transition-colors duration-300"
              />
              <span class="text-sm font-semibold text-gray-500 group-hover:text-gray-800 transition-colors duration-300">
                {{ company.name }}
              </span>
            </div>
          </div>
        </div>
        
        <!-- Gradient overlays for smooth edges -->
        <div class="absolute top-0 left-0 w-20 h-full bg-gradient-to-r from-white to-transparent pointer-events-none"></div>
        <div class="absolute top-0 right-0 w-20 h-full bg-gradient-to-l from-white to-transparent pointer-events-none"></div>
      </div>

      <!-- Interactive Stats -->
      <div class="mt-12 grid grid-cols-2 md:grid-cols-4 gap-8 text-center">
        <div class="stat-counter">
          <div class="text-2xl font-bold text-gray-900 mb-1" ref="counter1">0</div>
          <div class="text-sm text-gray-600">Companies Trust Us</div>
        </div>
        <div class="stat-counter">
          <div class="text-2xl font-bold text-gray-900 mb-1" ref="counter2">0</div>
          <div class="text-sm text-gray-600">Countries Worldwide</div>
        </div>
        <div class="stat-counter">
          <div class="text-2xl font-bold text-gray-900 mb-1" ref="counter3">0</div>
          <div class="text-sm text-gray-600">Years of Excellence</div>
        </div>
        <div class="stat-counter">
          <div class="text-2xl font-bold text-gray-900 mb-1" ref="counter4">0</div>
          <div class="text-sm text-gray-600">Success Rate</div>
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
  BuildingOfficeIcon,
  CloudIcon,
  CpuChipIcon,
  DevicePhoneMobileIcon,
  GlobeAltIcon,
  RocketLaunchIcon,
  ShieldCheckIcon,
  SparklesIcon
} from '@heroicons/vue/24/outline'

// Fallback to Heroicons for a more reliable approach
const companies = [
  { name: 'Microsoft', icon: BuildingOfficeIcon },
  { name: 'Google', icon: GlobeAltIcon },
  { name: 'Amazon', icon: CloudIcon },
  { name: 'Apple', icon: DevicePhoneMobileIcon },
  { name: 'Meta', icon: SparklesIcon },
  { name: 'Netflix', icon: RocketLaunchIcon },
  { name: 'Spotify', icon: CpuChipIcon },
  { name: 'Adobe', icon: ShieldCheckIcon },
  { name: 'Tesla', icon: BuildingOfficeIcon },
  { name: 'Uber', icon: GlobeAltIcon },
  { name: 'Airbnb', icon: CloudIcon },
  { name: 'Dropbox', icon: DevicePhoneMobileIcon }
]

const logoSlider = ref(null)
const counter1 = ref(null)
const counter2 = ref(null)
const counter3 = ref(null)
const counter4 = ref(null)

onMounted(() => {
  if (process.client) {
    gsap.registerPlugin(ScrollTrigger)

    // Pause animation on hover
    const sliderElement = logoSlider.value
    if (sliderElement) {
      sliderElement.addEventListener('mouseenter', () => {
        sliderElement.style.animationPlayState = 'paused'
      })
      
      sliderElement.addEventListener('mouseleave', () => {
        sliderElement.style.animationPlayState = 'running'
      })
    }

    // Animate counters when section comes into view
    const animateCounters = () => {
      gsap.to(counter1.value, {
        innerHTML: 500,
        duration: 2,
        ease: 'power2.out',
        snap: { innerHTML: 1 },
        onUpdate: function() {
          counter1.value.innerHTML = Math.ceil(counter1.value.innerHTML) + '+'
        }
      })

      gsap.to(counter2.value, {
        innerHTML: 25,
        duration: 2,
        ease: 'power2.out',
        snap: { innerHTML: 1 },
        onUpdate: function() {
          counter2.value.innerHTML = Math.ceil(counter2.value.innerHTML) + '+'
        }
      })

      gsap.to(counter3.value, {
        innerHTML: 15,
        duration: 2,
        ease: 'power2.out',
        snap: { innerHTML: 1 },
        onUpdate: function() {
          counter3.value.innerHTML = Math.ceil(counter3.value.innerHTML) + '+'
        }
      })

      gsap.to(counter4.value, {
        innerHTML: 98,
        duration: 2,
        ease: 'power2.out',
        snap: { innerHTML: 1 },
        onUpdate: function() {
          counter4.value.innerHTML = Math.ceil(counter4.value.innerHTML) + '%'
        }
      })
    }

    // Trigger counter animation when section is visible
    ScrollTrigger.create({
      trigger: '.stat-counter',
      start: 'top 80%',
      onEnter: animateCounters,
      once: true
    })
  }
})
</script>

<style scoped>
@keyframes slide {
  0% {
    transform: translateX(0);
  }
  100% {
    transform: translateX(-50%);
  }
}

.animate-slide {
  animation: slide 30s linear infinite;
}

.company-logo:hover {
  transform: scale(1.1);
}
</style>