<template>
  <section class="min-h-screen bg-white flex items-start justify-center pt-24 md:pt-36">
    <div class="w-full max-w-7xl mx-auto pl-0 pr-4 sm:pl-0 sm:pr-6 lg:pl-2 lg:pr-8">
      <div class="grid lg:grid-cols-2 gap-12 items-start">
        <!-- Left Content -->
        <div class="hero-content pl-4 sm:pl-6 lg:pl-4">
          <!-- Badge -->
          <div class="inline-flex items-center bg-gray-100 text-gray-700 px-2 py-2 rounded-full text-sm font-medium mb-6">
            <CheckCircleIcon class="w-3 h-3 text-green-500 mr-2" />
            Trusted by Fortune 500 Companies
          </div>

          <h1 class="text-5xl md:text-6xl lg:text-7xl font-bold mb-6 leading-tight text-gray-900">
            <span class="block">Enterprise-grade</span>
            <span class="block">digital transformation</span>
            <span class="block gradient-text">that delivers results.</span>
          </h1>
          
          <p class="text-md text-gray-600 leading-relaxed mb-8 max-w-2xl">
            We architect, build, and deploy scalable technology solutions that transform how enterprises operate. 
            From cloud migration to AI integration, we deliver measurable business outcomes with 98% client satisfaction.
          </p>

          <div class="space-y-8">
            <div class="bg-white p-6 rounded-2xl border border-gray-600 hover:border-gray-900 transition-all duration-300">
              <div class="flex items-center justify-between mb-4">
                <div>
                  <div class="text-gray-900 font-semibold text-base">Recent Success</div>
                  <div class="text-gray-500 text-sm">Manufacturing Corp</div>
                </div>
                <div class="text-right">
                  <div class="text-gray-900 font-bold text-xl">+300%</div>
                  <div class="text-gray-500 text-xs">Efficiency</div>
                </div>
              </div>
              
              <div class="flex items-center justify-between">
                <div class="flex items-center space-x-3">
                  <div class="flex -space-x-1">
                    <div class="w-8 h-8 bg-gray-200 rounded-full border-2 border-white flex items-center justify-center">
                      <span class="text-gray-600 font-medium text-xs">JD</span>
                    </div>
                    <div class="w-8 h-8 bg-gray-300 rounded-full border-2 border-white flex items-center justify-center">
                      <span class="text-gray-700 font-medium text-xs">MK</span>
                    </div>
                    <div class="w-8 h-8 bg-gray-400 rounded-full border-2 border-white flex items-center justify-center">
                      <span class="text-white font-medium text-xs">SP</span>
                    </div>
                  </div>
                  <div>
                    <div class="text-gray-900 font-medium text-sm">Executive Team</div>
                  </div>
                </div>
                
                <div class="w-2 h-2 bg-green-500 rounded-full"></div>
              </div>
            </div>
            
            <div class="flex flex-col sm:flex-row items-start gap-4">
              <button class="btn-primary text-md px-10 py-4 shadow-lg">
                Schedule Free Consultation →
              </button>
              <button class="btn-secondary text-md px-10 py-4">
                View Case Studies
              </button>
            </div>
          </div>

          <!-- Trust Indicators -->
          <div class="flex flex-col sm:flex-row items-start sm:items-center space-y-4 sm:space-y-0 sm:space-x-8">
            <div class="flex items-center space-x-2">
              <div class="flex text-yellow-400">
                <StarIcon v-for="i in 5" :key="i" class="w-4 h-4 fill-current" />
              </div>
              <span class="text-gray-600 text-sm font-medium">4.9/5 (127 reviews)</span>
            </div>
            <div class="flex items-center space-x-2">
              <span class="text-2xl font-bold text-gray-900">$2.3B+</span>
              <span class="text-gray-600 text-sm">in client value generated</span>
            </div>
          </div>
        </div>
        
        <!-- Right Content -->
        <div class="hero-right">
          <!-- Main Card - Enhanced Prominence -->
          <div class="bg-white rounded-2xl p-10 border-2 border-gray-200 mb-6 shadow-lg hover:shadow-xl transition-all duration-300">
            <div class="text-center mb-10">
              <div class="inline-flex items-center bg-gray-900 text-white px-4 py-2 rounded-full text-xs font-semibold mb-4 tracking-wide">
                ENTERPRISE SOLUTIONS
              </div>
              <h3 class="text-3xl font-bold text-gray-900 mb-4 font-heading">
                Solutions That Scale With You
              </h3>
              <p class="text-gray-600 font-body text-base leading-relaxed">
                Enterprise-grade technology solutions designed for sustainable growth and digital transformation.
              </p>
            </div>
            
            <!-- Minimal Services List with Enhanced Animations -->
            <div class="space-y-4 mb-8">
              <div class="service-item flex items-center space-x-4 p-4 rounded-xl hover:bg-gray-50 transition-all duration-300 cursor-pointer group">
                <div class="w-10 h-10 bg-gray-100 rounded-lg flex items-center justify-center group-hover:bg-blue-50 transition-all duration-300 group-hover:scale-110">
                  <CloudIcon class="w-5 h-5 text-gray-600 group-hover:text-blue-600 transition-all duration-300 group-hover:rotate-3" />
                </div>
                <div class="flex-1">
                  <div class="text-gray-900 font-semibold text-sm group-hover:text-blue-900 transition-colors duration-300">Cloud Migration</div>
                  <div class="text-gray-500 text-xs group-hover:text-blue-600 transition-colors duration-300">AWS • Azure • GCP</div>
                </div>
                <div class="w-0 group-hover:w-4 transition-all duration-300 overflow-hidden">
                  <div class="text-blue-600 text-sm">→</div>
                </div>
              </div>
              
              <div class="service-item flex items-center space-x-4 p-4 rounded-xl hover:bg-gray-50 transition-all duration-300 cursor-pointer group">
                <div class="w-10 h-10 bg-gray-100 rounded-lg flex items-center justify-center group-hover:bg-purple-50 transition-all duration-300 group-hover:scale-110">
                  <CpuChipIcon class="w-5 h-5 text-gray-600 group-hover:text-purple-600 transition-all duration-300 group-hover:-rotate-3" />
                </div>
                <div class="flex-1">
                  <div class="text-gray-900 font-semibold text-sm group-hover:text-purple-900 transition-colors duration-300">AI Integration</div>
                  <div class="text-gray-500 text-xs group-hover:text-purple-600 transition-colors duration-300">ML • Automation • Analytics</div>
                </div>
                <div class="w-0 group-hover:w-4 transition-all duration-300 overflow-hidden">
                  <div class="text-purple-600 text-sm">→</div>
                </div>
              </div>
              
              <div class="service-item flex items-center space-x-4 p-4 rounded-xl hover:bg-gray-50 transition-all duration-300 cursor-pointer group">
                <div class="w-10 h-10 bg-gray-100 rounded-lg flex items-center justify-center group-hover:bg-green-50 transition-all duration-300 group-hover:scale-110">
                  <DevicePhoneMobileIcon class="w-5 h-5 text-gray-600 group-hover:text-green-600 transition-all duration-300 group-hover:rotate-6" />
                </div>
                <div class="flex-1">
                  <div class="text-gray-900 font-semibold text-sm group-hover:text-green-900 transition-colors duration-300">App Development</div>
                  <div class="text-gray-500 text-xs group-hover:text-green-600 transition-colors duration-300">Web • Mobile • API</div>
                </div>
                <div class="w-0 group-hover:w-4 transition-all duration-300 overflow-hidden">
                  <div class="text-green-600 text-sm">→</div>
                </div>
              </div>
              
              <div class="service-item flex items-center space-x-4 p-4 rounded-xl hover:bg-gray-50 transition-all duration-300 cursor-pointer group">
                <div class="w-10 h-10 bg-gray-100 rounded-lg flex items-center justify-center group-hover:bg-orange-50 transition-all duration-300 group-hover:scale-110">
                  <LockClosedIcon class="w-5 h-5 text-gray-600 group-hover:text-orange-600 transition-all duration-300 group-hover:-rotate-6" />
                </div>
                <div class="flex-1">
                  <div class="text-gray-900 font-semibold text-sm group-hover:text-orange-900 transition-colors duration-300">Cybersecurity</div>
                  <div class="text-gray-500 text-xs group-hover:text-orange-600 transition-colors duration-300">Zero Trust • Compliance</div>
                </div>
                <div class="w-0 group-hover:w-4 transition-all duration-300 overflow-hidden">
                  <div class="text-orange-600 text-sm">→</div>
                </div>
              </div>
            </div>

            <!-- Enhanced Success Metrics -->
            <div class="bg-gray-900 text-white p-8 rounded-xl">
              <div class="grid grid-cols-3 gap-6 text-center">
                <div class="metric-item">
                  <div class="text-2xl font-bold mb-1 counter" data-target="98">0</div>
                  <div class="text-xs text-gray-300">Success Rate</div>
                </div>
                <div class="metric-item border-l border-r border-gray-700">
                  <div class="text-2xl font-bold mb-1">24/7</div>
                  <div class="text-xs text-gray-300">Support</div>
                </div>
                <div class="metric-item">
                  <div class="text-2xl font-bold mb-1 counter" data-target="15">0</div>
                  <div class="text-xs text-gray-300">Years Exp.</div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>

      <!-- Enhanced Interactive Stats Bar -->
      <div class="mt-16 pt-8 border-t border-gray-200">
        <div class="grid grid-cols-2 md:grid-cols-4 gap-8">
          <div class="stat-item text-center p-4 rounded-xl hover:bg-gray-50 transition-all duration-300 cursor-pointer group">
            <div class="text-3xl font-bold text-gray-900 mb-2 group-hover:text-blue-600 transition-colors duration-300 counter-stat" data-target="500">0</div>
            <div class="text-gray-600 text-sm group-hover:text-gray-800 transition-colors duration-300">Projects Delivered</div>
            <div class="w-0 group-hover:w-8 h-0.5 bg-blue-600 mx-auto mt-2 transition-all duration-300"></div>
          </div>
          
          <div class="stat-item text-center p-4 rounded-xl hover:bg-gray-50 transition-all duration-300 cursor-pointer group">
            <div class="text-3xl font-bold text-gray-900 mb-2 group-hover:text-purple-600 transition-colors duration-300 counter-stat" data-target="150">0</div>
            <div class="text-gray-600 text-sm group-hover:text-gray-800 transition-colors duration-300">Enterprise Clients</div>
            <div class="w-0 group-hover:w-8 h-0.5 bg-purple-600 mx-auto mt-2 transition-all duration-300"></div>
          </div>
          
          <div class="stat-item text-center p-4 rounded-xl hover:bg-gray-50 transition-all duration-300 cursor-pointer group">
            <div class="text-3xl font-bold text-gray-900 mb-2 group-hover:text-green-600 transition-colors duration-300 counter-stat" data-target="25">0</div>
            <div class="text-gray-600 text-sm group-hover:text-gray-800 transition-colors duration-300">Countries Served</div>
            <div class="w-0 group-hover:w-8 h-0.5 bg-green-600 mx-auto mt-2 transition-all duration-300"></div>
          </div>
          
          <div class="stat-item text-center p-4 rounded-xl hover:bg-gray-50 transition-all duration-300 cursor-pointer group">
            <div class="text-3xl font-bold text-gray-900 mb-2 group-hover:text-orange-600 transition-colors duration-300">
              <span class="counter-stat" data-target="99.9">0</span>%
            </div>
            <div class="text-gray-600 text-sm group-hover:text-gray-800 transition-colors duration-300">Uptime SLA</div>
            <div class="w-0 group-hover:w-8 h-0.5 bg-orange-600 mx-auto mt-2 transition-all duration-300"></div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
import { onMounted } from 'vue'
import { gsap } from 'gsap'
import {
  CheckCircleIcon,
  BoltIcon,
  CheckIcon,
  ShieldCheckIcon,
  StarIcon,
  CloudIcon,
  CpuChipIcon,
  DevicePhoneMobileIcon,
  LockClosedIcon
} from '@heroicons/vue/24/outline'

onMounted(() => {
  if (process.client) {
    // Enhanced animations with more elements
    gsap.fromTo('.hero-content', 
      { opacity: 0, y: 50 },
      { opacity: 1, y: 0, duration: 1, ease: 'power3.out' }
    )
    
    gsap.fromTo('.hero-right', 
      { opacity: 0, x: 50 },
      { opacity: 1, x: 0, duration: 1, delay: 0.3, ease: 'power3.out' }
    )

    // Animate the key benefits
    gsap.fromTo('.hero-content .grid div', 
      { opacity: 0, y: 20 },
      { opacity: 1, y: 0, duration: 0.6, delay: 0.8, stagger: 0.1, ease: 'power3.out' }
    )

    // Animate service items with stagger
    gsap.fromTo('.service-item', 
      { opacity: 0, y: 30, scale: 0.9 },
      { 
        opacity: 1, 
        y: 0, 
        scale: 1,
        duration: 0.6, 
        delay: 1.2, 
        stagger: 0.1, 
        ease: 'back.out(1.7)' 
      }
    )

    // Counter animation for metrics
    const animateCounter = (element, target) => {
      gsap.to(element, {
        innerHTML: target,
        duration: 2,
        delay: 1.5,
        ease: 'power2.out',
        snap: { innerHTML: 1 },
        onUpdate: function() {
          element.innerHTML = Math.ceil(element.innerHTML) + (target === 98 ? '%' : '+')
        }
      })
    }

    // Initialize counters
    const counters = document.querySelectorAll('.counter')
    counters.forEach(counter => {
      const target = parseInt(counter.dataset.target)
      animateCounter(counter, target)
    })

    // Add click handlers for service items
    const serviceItems = document.querySelectorAll('.service-item')
    serviceItems.forEach(item => {
      item.addEventListener('click', () => {
        // Add a subtle pulse animation on click
        gsap.to(item, {
          scale: 0.95,
          duration: 0.1,
          yoyo: true,
          repeat: 1,
          ease: 'power2.inOut'
        })
      })
    })

    // Animate metric items on hover
    const metricItems = document.querySelectorAll('.metric-item')
    metricItems.forEach(item => {
      item.addEventListener('mouseenter', () => {
        gsap.to(item, {
          scale: 1.05,
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

    // Enhanced stats bar animation
    const statItems = document.querySelectorAll('.stat-item')
    statItems.forEach(item => {
      const counterStat = item.querySelector('.counter-stat')
      const target = parseInt(counterStat.dataset.target)

      // Initial state
      gsap.set(counterStat, { innerHTML: 0 })

      item.addEventListener('mouseenter', () => {
        // Scale up on hover
        gsap.to(item, {
          scale: 1.05,
          duration: 0.3,
          ease: 'power2.out'
        })

        // Animate counter
        animateCounter(counterStat, target)

        // Underline animation
        gsap.to(item.querySelector('div.w-0'), {
          width: '100%',
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

        // Reset counter
        gsap.to(counterStat, {
          innerHTML: 0,
          duration: 0.1,
          ease: 'power2.out'
        })

        // Reset underline
        gsap.to(item.querySelector('div.w-0'), {
          width: 0,
          duration: 0.3,
          ease: 'power2.out'
        })
      })
    })
  }
})
</script>