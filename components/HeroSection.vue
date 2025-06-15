<template>
  <section class="min-h-screen bg-white flex items-center justify-center pt-20">
    <div class="container-custom">
      <div class="grid lg:grid-cols-2 gap-12 items-center">
        <!-- Left Content -->
        <div class="hero-content">
          <h1 class="text-5xl md:text-6xl lg:text-7xl font-bold mb-6 leading-tight text-gray-900">
            <span class="block">Digital transformation</span>
            <span class="block">solutions for</span>
            <span class="block gradient-text">enterprises.</span>
          </h1>
          
          <p class="text-xl text-gray-600 leading-relaxed mb-8 max-w-2xl">
            We are the catalyst for your enterprise's digital evolution, delivering 
            cutting-edge technology solutions that drive growth and efficiency.
          </p>
          
          <div class="flex flex-col sm:flex-row items-start gap-4 mb-12">
            <button class="btn-primary text-lg px-10 py-4">
              Book a strategy call →
            </button>
            <button class="btn-secondary text-lg px-10 py-4">
              Get a custom quote
            </button>
          </div>
          
          <div class="text-center sm:text-left">
            <p class="text-gray-500 font-medium mb-4">Trusted by 500+ global companies</p>
          </div>
        </div>
        
        <!-- Right Content -->
        <div class="hero-right">
          <div class="bg-gray-50 rounded-2xl p-8 border border-gray-100">
            <div class="text-center mb-8">
              <h3 class="text-2xl font-bold text-gray-900 mb-4">
                We deliver globally enterprise solutions
              </h3>
              <p class="text-gray-600">
                Smoothly, without delay, saving your time and money with an efficient process.
              </p>
            </div>
            
            <div class="flex items-center justify-center space-x-4 mb-6">
              <div class="flex -space-x-2">
                <div class="w-10 h-10 bg-gray-300 rounded-full border-2 border-white flex items-center justify-center">
                  <span class="text-sm font-semibold">👤</span>
                </div>
                <div class="w-10 h-10 bg-gray-400 rounded-full border-2 border-white flex items-center justify-center">
                  <span class="text-sm font-semibold">👤</span>
                </div>
                <div class="w-10 h-10 bg-gray-500 rounded-full border-2 border-white flex items-center justify-center">
                  <span class="text-sm font-semibold">👤</span>
                </div>
              </div>
              <div class="text-left">
                <p class="text-sm font-semibold text-gray-900">Loved by 500+</p>
                <p class="text-sm text-gray-600">Founders</p>
              </div>
              <div class="flex items-center space-x-1">
                <div class="flex text-yellow-400">
                  <span>★★★★★</span>
                </div>
                <span class="text-sm text-gray-600">10 REVIEWS</span>
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

onMounted(() => {
  if (process.client) {
    gsap.fromTo('.hero-content', 
      { opacity: 0, y: 50 },
      { opacity: 1, y: 0, duration: 1, ease: 'power3.out' }
    )
    
    gsap.fromTo('.hero-right', 
      { opacity: 0, x: 50 },
      { opacity: 1, x: 0, duration: 1, delay: 0.3, ease: 'power3.out' }
    )
  }
})
</script>