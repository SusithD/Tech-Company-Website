<template>
  <section class="min-h-screen bg-white flex items-center justify-center pt-32 md:pt-36">
    <div class="container-custom">
      <div class="grid lg:grid-cols-2 gap-12 items-center">
        <!-- Left Content -->
        <div class="hero-content">
          <!-- Badge -->
          <div class="inline-flex items-center bg-gray-100 text-gray-700 px-4 py-2 rounded-full text-sm font-medium mb-6">
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

          <!-- Key Benefits -->
          <div class="grid grid-cols-1 sm:grid-cols-3 gap-4 mb-8">
            <div class="flex items-center space-x-2">
              <div class="w-8 h-8 bg-blue-100 rounded-full flex items-center justify-center">
                <BoltIcon class="w-4 h-4 text-blue-600" />
              </div>
              <div>
                <div class="text-gray-900 font-semibold text-sm">Fast Delivery</div>
                <div class="text-gray-600 text-xs">30% faster than industry average</div>
              </div>
            </div>
            <div class="flex items-center space-x-2">
              <div class="w-8 h-8 bg-green-100 rounded-full flex items-center justify-center">
                <CheckIcon class="w-4 h-4 text-green-600" />
              </div>
              <div>
                <div class="text-gray-900 font-semibold text-sm">Proven Results</div>
                <div class="text-gray-600 text-xs">500+ successful projects</div>
              </div>
            </div>
            <div class="flex items-center space-x-2">
              <div class="w-8 h-8 bg-purple-100 rounded-full flex items-center justify-center">
                <ShieldCheckIcon class="w-4 h-4 text-purple-600" />
              </div>
              <div>
                <div class="text-gray-900 font-semibold text-sm">Enterprise Security</div>
                <div class="text-gray-600 text-xs">SOC 2 & ISO certified</div>
              </div>
            </div>
          </div>
          
          <div class="flex flex-col sm:flex-row items-start gap-4 mb-8">
            <button class="btn-primary text-md px-10 py-4 shadow-lg">
              Schedule Free Consultation →
            </button>
            <button class="btn-secondary text-md px-10 py-4">
              View Case Studies
            </button>
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
          <!-- Main Card -->
          <div class="bg-gray-50 rounded-2xl p-8 border border-gray-100 mb-6">
            <div class="text-center mb-6">
              <h3 class="text-2xl font-bold text-gray-900 mb-2">
                Enterprise Solutions That Scale
              </h3>
              <p class="text-gray-600">
                From startup to Fortune 500, we deliver technology solutions that grow with your business.
              </p>
            </div>
            
            <!-- Services Grid -->
            <div class="grid grid-cols-2 gap-4 mb-6">
              <div class="bg-white p-4 rounded-xl border border-gray-200">
                <div class="w-8 h-8 bg-blue-100 rounded-lg flex items-center justify-center mb-3">
                  <CloudIcon class="w-4 h-4 text-blue-600" />
                </div>
                <div class="text-gray-900 font-semibold text-sm mb-1">Cloud Migration</div>
                <div class="text-gray-600 text-xs">AWS, Azure, GCP</div>
              </div>
              <div class="bg-white p-4 rounded-xl border border-gray-200">
                <div class="w-8 h-8 bg-purple-100 rounded-lg flex items-center justify-center mb-3">
                  <CpuChipIcon class="w-4 h-4 text-purple-600" />
                </div>
                <div class="text-gray-900 font-semibold text-sm mb-1">AI Integration</div>
                <div class="text-gray-600 text-xs">ML, Automation</div>
              </div>
              <div class="bg-white p-4 rounded-xl border border-gray-200">
                <div class="w-8 h-8 bg-green-100 rounded-lg flex items-center justify-center mb-3">
                  <DevicePhoneMobileIcon class="w-4 h-4 text-green-600" />
                </div>
                <div class="text-gray-900 font-semibold text-sm mb-1">App Development</div>
                <div class="text-gray-600 text-xs">Web, Mobile, API</div>
              </div>
              <div class="bg-white p-4 rounded-xl border border-gray-200">
                <div class="w-8 h-8 bg-orange-100 rounded-lg flex items-center justify-center mb-3">
                  <LockClosedIcon class="w-4 h-4 text-orange-600" />
                </div>
                <div class="text-gray-900 font-semibold text-sm mb-1">Cybersecurity</div>
                <div class="text-gray-600 text-xs">Zero Trust, SOC</div>
              </div>
            </div>

            <!-- Client Success Metrics -->
            <div class="bg-gradient-to-r from-blue-600 to-purple-600 text-white p-4 rounded-xl">
              <div class="grid grid-cols-3 gap-4 text-center">
                <div>
                  <div class="text-2xl font-bold">98%</div>
                  <div class="text-xs opacity-90">Success Rate</div>
                </div>
                <div>
                  <div class="text-2xl font-bold">24/7</div>
                  <div class="text-xs opacity-90">Support</div>
                </div>
                <div>
                  <div class="text-2xl font-bold">15+</div>
                  <div class="text-xs opacity-90">Years Experience</div>
                </div>
              </div>
            </div>
          </div>

          <!-- Secondary Trust Card -->
          <div class="bg-white p-6 rounded-2xl border border-gray-200 shadow-sm">
            <div class="flex items-center justify-between mb-4">
              <div>
                <div class="text-gray-900 font-bold text-lg">Recent Success</div>
                <div class="text-gray-600 text-sm">Global Manufacturing Corp</div>
              </div>
              <div class="text-right">
                <div class="text-green-600 font-bold text-xl">+300%</div>
                <div class="text-gray-600 text-xs">Efficiency Gain</div>
              </div>
            </div>
            <div class="flex items-center space-x-3">
              <div class="flex -space-x-2">
                <div class="w-8 h-8 bg-gradient-to-r from-blue-600 to-purple-600 rounded-full border-2 border-white flex items-center justify-center">
                  <span class="text-white font-bold text-xs">JD</span>
                </div>
                <div class="w-8 h-8 bg-gradient-to-r from-purple-600 to-blue-800 rounded-full border-2 border-white flex items-center justify-center">
                  <span class="text-white font-bold text-xs">MK</span>
                </div>
                <div class="w-8 h-8 bg-gradient-to-r from-blue-800 to-blue-600 rounded-full border-2 border-white flex items-center justify-center">
                  <span class="text-white font-bold text-xs">SP</span>
                </div>
              </div>
              <div class="text-left">
                <div class="text-gray-900 font-semibold text-sm">C-Level Team</div>
                <div class="text-gray-600 text-xs">Direct stakeholder engagement</div>
              </div>
            </div>
          </div>
        </div>
      </div>

      <!-- Bottom Stats Bar -->
      <div class="mt-16 pt-8 border-t border-gray-200">
        <div class="grid grid-cols-2 md:grid-cols-4 gap-8 text-center">
          <div>
            <div class="text-3xl font-bold text-gray-900 mb-2">500+</div>
            <div class="text-gray-600 text-sm">Projects Delivered</div>
          </div>
          <div>
            <div class="text-3xl font-bold text-gray-900 mb-2">150+</div>
            <div class="text-gray-600 text-sm">Enterprise Clients</div>
          </div>
          <div>
            <div class="text-3xl font-bold text-gray-900 mb-2">25+</div>
            <div class="text-gray-600 text-sm">Countries Served</div>
          </div>
          <div>
            <div class="text-3xl font-bold text-gray-900 mb-2">99.9%</div>
            <div class="text-gray-600 text-sm">Uptime SLA</div>
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
  }
})
</script>