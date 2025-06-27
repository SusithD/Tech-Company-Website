<template>
  <section class="min-h-screen bg-gradient-to-br from-gray-50 via-white to-gray-50 flex items-center justify-center pt-24 md:pt-36 relative overflow-hidden">
    <!-- Background Pattern -->
    <div class="absolute inset-0 opacity-5">
      <div class="absolute inset-0" style="background-image: radial-gradient(circle at 25% 75%, rgba(59, 130, 246, 0.1) 0%, transparent 50%), radial-gradient(circle at 75% 25%, rgba(147, 51, 234, 0.1) 0%, transparent 50%);"></div>
    </div>

    <!-- Floating Elements -->
    <div class="absolute inset-0 opacity-10">
      <div class="hero-float hero-float-1"></div>
      <div class="hero-float hero-float-2"></div>
      <div class="hero-float hero-float-3"></div>
    </div>

    <div class="container-custom relative z-10">
      <div class="max-w-6xl mx-auto text-center">
        <!-- Badge -->
        <div class="inline-flex items-center bg-blue-100 text-blue-800 px-6 py-3 rounded-full text-sm font-semibold mb-8 animate-pulse">
          <span class="w-2 h-2 bg-blue-500 rounded-full mr-3"></span>
          ABOUT MB TECH NOW
        </div>

        <!-- Main Headline -->
        <h1 class="text-6xl md:text-7xl lg:text-8xl font-bold mb-8 text-gray-900 font-heading leading-tight">
          Architecting
          <span class="block gradient-text animate-gradient">Tomorrow's</span>
          <span class="block text-5xl md:text-6xl lg:text-7xl text-gray-700">Enterprise Solutions</span>
        </h1>

        <p class="text-2xl md:text-3xl text-gray-600 leading-relaxed max-w-5xl mx-auto font-light mb-12">
          Since 2009, we've been the <span class="font-semibold text-gray-800">strategic technology partner</span> 
          that Fortune 500 companies trust to transform their digital landscapes and 
          <span class="font-semibold gradient-text">accelerate their success</span>.
        </p>

        <!-- Key Stats -->
        <div class="grid grid-cols-2 md:grid-cols-4 gap-8 mb-16">
          <div class="stat-item group cursor-pointer">
            <div class="text-4xl md:text-5xl font-bold text-gray-900 mb-2 group-hover:text-blue-600 transition-colors duration-300 counter" data-target="15">0</div>
            <div class="text-gray-600 font-medium">Years of Excellence</div>
          </div>
          <div class="stat-item group cursor-pointer">
            <div class="text-4xl md:text-5xl font-bold text-gray-900 mb-2 group-hover:text-green-600 transition-colors duration-300 counter" data-target="500">0</div>
            <div class="text-gray-600 font-medium">Projects Delivered</div>
          </div>
          <div class="stat-item group cursor-pointer">
            <div class="text-4xl md:text-5xl font-bold text-gray-900 mb-2 group-hover:text-purple-600 transition-colors duration-300 counter" data-target="150">0</div>
            <div class="text-gray-600 font-medium">Enterprise Clients</div>
          </div>
          <div class="stat-item group cursor-pointer">
            <div class="text-4xl md:text-5xl font-bold text-gray-900 mb-2 group-hover:text-orange-600 transition-colors duration-300 counter" data-target="25">0</div>
            <div class="text-gray-600 font-medium">Countries Served</div>
          </div>
        </div>

        <!-- CTA Buttons -->
        <div class="flex flex-col sm:flex-row items-center justify-center gap-6">
          <button class="inline-flex items-center bg-gray-900 text-white px-8 py-4 rounded-full font-semibold hover:bg-gray-800 transition-all duration-300 transform hover:scale-105 shadow-lg">
            <span>Our Story</span>
            <svg class="w-5 h-5 ml-2" fill="none" stroke="currentColor" viewBox="0 0 24 24">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 14l-7 7m0 0l-7-7m7 7V3"></path>
            </svg>
          </button>
          <button class="inline-flex items-center border-2 border-gray-900 text-gray-900 px-8 py-4 rounded-full font-semibold hover:bg-gray-900 hover:text-white transition-all duration-300">
            <span>Meet Our Team</span>
            <svg class="w-5 h-5 ml-2" fill="none" stroke="currentColor" viewBox="0 0 24 24">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M17 8l4 4m0 0l-4 4m4-4H3"></path>
            </svg>
          </button>
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
    
    // Floating animations
    gsap.to('.hero-float-1', { y: -20, duration: 3, yoyo: true, repeat: -1, ease: 'sine.inOut' })
    gsap.to('.hero-float-2', { y: -30, duration: 4, yoyo: true, repeat: -1, ease: 'sine.inOut', delay: 1 })
    gsap.to('.hero-float-3', { y: -25, duration: 3.5, yoyo: true, repeat: -1, ease: 'sine.inOut', delay: 2 })
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

.hero-float {
  position: absolute;
  width: 12px;
  height: 12px;
  background: linear-gradient(45deg, #3b82f6, #10b981);
  border-radius: 50%;
  opacity: 0.6;
}

.hero-float-1 { top: 15%; left: 5%; }
.hero-float-2 { top: 60%; right: 10%; }
.hero-float-3 { bottom: 25%; left: 15%; }
</style>