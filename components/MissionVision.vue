<template>
  <section class="section-padding bg-gradient-to-br from-gray-50 via-white to-gray-50 relative overflow-hidden">
    <!-- Background Pattern -->
    <div class="absolute inset-0 opacity-5">
      <div class="absolute inset-0" style="background-image: radial-gradient(circle at 25% 75%, rgba(59, 130, 246, 0.1) 0%, transparent 50%), radial-gradient(circle at 75% 25%, rgba(147, 51, 234, 0.1) 0%, transparent 50%);"></div>
    </div>

    <div class="container-custom relative z-10">
      <!-- Header -->
      <div class="max-w-4xl mx-auto text-center mb-20">
        <div class="inline-flex items-center bg-purple-100 text-purple-800 px-6 py-3 rounded-full text-sm font-semibold mb-8">
          <span class="w-2 h-2 bg-purple-500 rounded-full mr-3"></span>
          MISSION & VISION
        </div>
        
        <h2 class="text-5xl md:text-6xl lg:text-7xl font-bold mb-8 text-gray-900 font-heading leading-tight">
          Driving
          <span class="block gradient-text animate-gradient">Digital</span>
          <span class="block text-4xl md:text-5xl lg:text-6xl text-gray-700">Excellence</span>
        </h2>
        
        <p class="text-xl text-gray-600 leading-relaxed">
          Our purpose is to empower enterprises with transformative technology solutions 
          that drive sustainable growth and competitive advantage.
        </p>
      </div>

      <!-- Mission & Vision Cards -->
      <div class="grid lg:grid-cols-2 gap-12 mb-20">
        <!-- Mission Card -->
        <div class="mission-card group relative bg-white p-12 rounded-3xl border border-gray-200 hover:border-blue-300 transition-all duration-500 cursor-pointer overflow-hidden">
          <div class="absolute inset-0 bg-gradient-to-br from-blue-50 to-purple-50 opacity-0 group-hover:opacity-100 transition-opacity duration-500"></div>
          
          <div class="relative z-10">
            <div class="flex items-center space-x-4 mb-8">
              <div class="w-16 h-16 bg-blue-100 rounded-2xl flex items-center justify-center group-hover:bg-blue-200 group-hover:scale-110 transition-all duration-500">
                <svg class="w-8 h-8 text-blue-600" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M13 10V3L4 14h7v7l9-11h-7z"></path>
                </svg>
              </div>
              <div>
                <h3 class="text-3xl font-bold text-gray-900 group-hover:text-blue-900 transition-colors duration-300 font-heading">Our Mission</h3>
                <div class="text-blue-600 font-medium">What We Do</div>
              </div>
            </div>
            
            <p class="text-lg text-gray-600 leading-relaxed mb-8 group-hover:text-gray-700 transition-colors duration-300">
              To <span class="font-semibold text-gray-800">architect and implement cutting-edge technology solutions</span> 
              that transform enterprises, streamline operations, and accelerate digital innovation. We bridge the gap 
              between complex technology and business success.
            </p>
            
            <!-- Mission Points -->
            <div class="space-y-4">
              <div class="flex items-start space-x-3">
                <div class="w-2 h-2 bg-blue-600 rounded-full mt-2 flex-shrink-0"></div>
                <div class="text-gray-700">Enable digital transformation at enterprise scale</div>
              </div>
              <div class="flex items-start space-x-3">
                <div class="w-2 h-2 bg-blue-600 rounded-full mt-2 flex-shrink-0"></div>
                <div class="text-gray-700">Deliver measurable ROI through strategic technology partnerships</div>
              </div>
              <div class="flex items-start space-x-3">
                <div class="w-2 h-2 bg-blue-600 rounded-full mt-2 flex-shrink-0"></div>
                <div class="text-gray-700">Provide 24/7 enterprise-grade support and innovation</div>
              </div>
            </div>
          </div>
        </div>

        <!-- Vision Card -->
        <div class="vision-card group relative bg-white p-12 rounded-3xl border border-gray-200 hover:border-purple-300 transition-all duration-500 cursor-pointer overflow-hidden">
          <div class="absolute inset-0 bg-gradient-to-br from-purple-50 to-green-50 opacity-0 group-hover:opacity-100 transition-opacity duration-500"></div>
          
          <div class="relative z-10">
            <div class="flex items-center space-x-4 mb-8">
              <div class="w-16 h-16 bg-purple-100 rounded-2xl flex items-center justify-center group-hover:bg-purple-200 group-hover:scale-110 transition-all duration-500">
                <svg class="w-8 h-8 text-purple-600" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M15 12a3 3 0 11-6 0 3 3 0 016 0z"></path>
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M2.458 12C3.732 7.943 7.523 5 12 5c4.478 0 8.268 2.943 9.542 7-1.274 4.057-5.064 7-9.542 7-4.477 0-8.268-2.943-9.542-7z"></path>
                </svg>
              </div>
              <div>
                <h3 class="text-3xl font-bold text-gray-900 group-hover:text-purple-900 transition-colors duration-300 font-heading">Our Vision</h3>
                <div class="text-purple-600 font-medium">Where We're Going</div>
              </div>
            </div>
            
            <p class="text-lg text-gray-600 leading-relaxed mb-8 group-hover:text-gray-700 transition-colors duration-300">
              To be the <span class="font-semibold text-gray-800">global leader in enterprise digital transformation</span>, 
              recognized for innovation, excellence, and the ability to turn visionary ideas into scalable, 
              business-critical solutions that define the future of industry.
            </p>
            
            <!-- Vision Points -->
            <div class="space-y-4">
              <div class="flex items-start space-x-3">
                <div class="w-2 h-2 bg-purple-600 rounded-full mt-2 flex-shrink-0"></div>
                <div class="text-gray-700">Pioneer next-generation enterprise technologies</div>
              </div>
              <div class="flex items-start space-x-3">
                <div class="w-2 h-2 bg-purple-600 rounded-full mt-2 flex-shrink-0"></div>
                <div class="text-gray-700">Empower 10,000+ enterprises globally by 2030</div>
              </div>
              <div class="flex items-start space-x-3">
                <div class="w-2 h-2 bg-purple-600 rounded-full mt-2 flex-shrink-0"></div>
                <div class="text-gray-700">Create the most trusted technology partnership ecosystem</div>
              </div>
            </div>
          </div>
        </div>
      </div>

      <!-- Impact Stats -->
      <div class="bg-gray-900 rounded-3xl p-12 text-white relative overflow-hidden">
        <div class="absolute inset-0 bg-gradient-to-r from-blue-600/20 to-purple-600/20 animate-pulse"></div>
        
        <div class="relative z-10 text-center">
          <h3 class="text-4xl md:text-5xl font-bold mb-6 font-heading">
            Transforming Industries Worldwide
          </h3>
          <p class="text-xl text-gray-300 mb-12 max-w-3xl mx-auto">
            Our mission-driven approach has generated measurable impact across enterprise clients globally
          </p>
          
          <div class="grid grid-cols-2 md:grid-cols-4 gap-8">
            <div class="impact-stat group cursor-pointer">
              <div class="text-4xl md:text-5xl font-bold text-blue-400 mb-2 group-hover:text-blue-300 transition-colors duration-300 counter" data-target="2.3">0</div>
              <div class="text-gray-300 font-medium">Billion+ Value Generated</div>
            </div>
            <div class="impact-stat group cursor-pointer">
              <div class="text-4xl md:text-5xl font-bold text-green-400 mb-2 group-hover:text-green-300 transition-colors duration-300 counter" data-target="98">0</div>
              <div class="text-gray-300 font-medium">% Client Satisfaction</div>
            </div>
            <div class="impact-stat group cursor-pointer">
              <div class="text-4xl md:text-5xl font-bold text-purple-400 mb-2 group-hover:text-purple-300 transition-colors duration-300 counter" data-target="300">0</div>
              <div class="text-gray-300 font-medium">% Average ROI</div>
            </div>
            <div class="impact-stat group cursor-pointer">
              <div class="text-4xl md:text-5xl font-bold text-orange-400 mb-2 group-hover:text-orange-300 transition-colors duration-300 counter" data-target="24">0</div>
              <div class="text-gray-300 font-medium">/7 Enterprise Support</div>
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
    
    // Animate mission card
    gsap.fromTo('.mission-card',
      { opacity: 0, x: -50 },
      {
        opacity: 1,
        x: 0,
        duration: 1,
        ease: 'power3.out',
        scrollTrigger: {
          trigger: '.mission-card',
          start: 'top 80%',
          toggleActions: 'play none none reverse'
        }
      }
    )
    
    // Animate vision card
    gsap.fromTo('.vision-card',
      { opacity: 0, x: 50 },
      {
        opacity: 1,
        x: 0,
        duration: 1,
        ease: 'power3.out',
        scrollTrigger: {
          trigger: '.vision-card',
          start: 'top 80%',
          toggleActions: 'play none none reverse'
        }
      }
    )
    
    // Animate impact stats
    gsap.fromTo('.impact-stat',
      { opacity: 0, y: 30 },
      {
        opacity: 1,
        y: 0,
        duration: 0.6,
        stagger: 0.15,
        ease: 'back.out(1.7)',
        scrollTrigger: {
          trigger: '.impact-stat',
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