<template>
  <section class="section-padding bg-white relative overflow-hidden">
    <!-- Background Pattern -->
    <div class="absolute inset-0 opacity-5">
      <div class="absolute inset-0" style="background-image: radial-gradient(circle at 20% 80%, rgba(59, 130, 246, 0.1) 0%, transparent 50%), radial-gradient(circle at 80% 20%, rgba(147, 51, 234, 0.1) 0%, transparent 50%);"></div>
    </div>

    <div class="container-custom relative z-10">
      <div class="grid lg:grid-cols-2 gap-16 items-center mb-20">
        <!-- Content Side -->
        <div class="story-content">
          <div class="inline-flex items-center bg-green-100 text-green-800 px-6 py-3 rounded-full text-sm font-semibold mb-8">
            <span class="w-2 h-2 bg-green-500 rounded-full mr-3"></span>
            OUR STORY
          </div>
          
          <h2 class="text-5xl md:text-6xl lg:text-7xl font-bold mb-8 text-gray-900 font-heading leading-tight">
            Born from
            <span class="block gradient-text animate-gradient">Innovation</span>
            <span class="block text-4xl md:text-5xl lg:text-6xl text-gray-700">& Ambition</span>
          </h2>
          
          <div class="space-y-6 text-lg text-gray-600 leading-relaxed">
            <p>
              <span class="font-semibold text-gray-800">The qexle began in 2009</span> with a simple yet powerful vision: 
              to bridge the gap between cutting-edge technology and business transformation. What started as a small team 
              of passionate engineers has evolved into a global leader in digital transformation.
            </p>
            
            <p>
              Our founders recognized that <span class="font-semibold text-gray-800">traditional IT approaches</span> 
              were holding enterprises back. They envisioned a future where technology would be the primary driver 
              of business growth, not just a support function.
            </p>
            
            <p>
              Today, we're proud to have <span class="gradient-text font-semibold">transformed over 500 enterprises</span> 
              across 25 countries, generating over $2.3 billion in client value through strategic technology partnerships.
            </p>
          </div>
          
          <!-- Key Milestones -->
          <div class="grid grid-cols-2 gap-6 mt-12">
            <div class="milestone-item group p-6 bg-gray-50 rounded-2xl hover:bg-blue-50 transition-all duration-300 cursor-pointer">
              <div class="text-3xl font-bold text-blue-600 mb-2 group-hover:scale-110 transition-transform duration-300">2009</div>
              <div class="text-gray-700 font-medium">Company Founded</div>
              <div class="text-sm text-gray-500 mt-1">Started with 3 engineers</div>
            </div>
            <div class="milestone-item group p-6 bg-gray-50 rounded-2xl hover:bg-green-50 transition-all duration-300 cursor-pointer">
              <div class="text-3xl font-bold text-green-600 mb-2 group-hover:scale-110 transition-transform duration-300">2015</div>
              <div class="text-gray-700 font-medium">Global Expansion</div>
              <div class="text-sm text-gray-500 mt-1">Opened offices in 5 countries</div>
            </div>
            <div class="milestone-item group p-6 bg-gray-50 rounded-2xl hover:bg-purple-50 transition-all duration-300 cursor-pointer">
              <div class="text-3xl font-bold text-purple-600 mb-2 group-hover:scale-110 transition-transform duration-300">2020</div>
              <div class="text-gray-700 font-medium">AI Leadership</div>
              <div class="text-sm text-gray-500 mt-1">Became AI transformation leader</div>
            </div>
            <div class="milestone-item group p-6 bg-gray-50 rounded-2xl hover:bg-orange-50 transition-all duration-300 cursor-pointer">
              <div class="text-3xl font-bold text-orange-600 mb-2 group-hover:scale-110 transition-transform duration-300">2025</div>
              <div class="text-gray-700 font-medium">Industry Pioneer</div>
              <div class="text-sm text-gray-500 mt-1">Fortune 500 trusted partner</div>
            </div>
          </div>
        </div>
        
        <!-- Visual Side -->
        <div class="story-visual relative">
          <!-- Main Image Card -->
          <div class="relative bg-white p-8 rounded-3xl shadow-lg border border-gray-200">
            <div class="aspect-w-16 aspect-h-12 bg-gradient-to-br from-blue-100 to-purple-100 rounded-2xl mb-6 flex items-center justify-center">
              <div class="text-center">
                <div class="w-20 h-20 bg-gray-900 rounded-2xl flex items-center justify-center mx-auto mb-4">
                  <span class="text-2xl font-bold text-white">MB</span>
                </div>
                <div class="text-gray-700 font-semibold">Our Journey</div>
              </div>
            </div>
            
            <!-- Growth Stats -->
            <div class="grid grid-cols-3 gap-4 text-center">
              <div class="growth-stat">
                <div class="text-2xl font-bold text-blue-600 counter" data-target="15">0</div>
                <div class="text-xs text-gray-500">Years</div>
              </div>
              <div class="growth-stat">
                <div class="text-2xl font-bold text-green-600 counter" data-target="150">0</div>
                <div class="text-xs text-gray-500">Clients</div>
              </div>
              <div class="growth-stat">
                <div class="text-2xl font-bold text-purple-600 counter" data-target="25">0</div>
                <div class="text-xs text-gray-500">Countries</div>
              </div>
            </div>
          </div>
          
          <!-- Floating Achievement Cards -->
          <div class="absolute -top-6 -right-6 bg-white p-4 rounded-2xl shadow-lg border border-gray-200 achievement-float">
            <div class="flex items-center space-x-3">
              <div class="w-8 h-8 bg-green-100 rounded-full flex items-center justify-center">
                <svg class="w-4 h-4 text-green-600" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 13l4 4L19 7"></path>
                </svg>
              </div>
              <div>
                <div class="text-sm font-semibold text-gray-900">98% Success Rate</div>
                <div class="text-xs text-gray-500">Project Delivery</div>
              </div>
            </div>
          </div>
          
          <div class="absolute -bottom-6 -left-6 bg-white p-4 rounded-2xl shadow-lg border border-gray-200 achievement-float">
            <div class="flex items-center space-x-3">
              <div class="w-8 h-8 bg-blue-100 rounded-full flex items-center justify-center">
                <svg class="w-4 h-4 text-blue-600" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M13 10V3L4 14h7v7l9-11h-7z"></path>
                </svg>
              </div>
              <div>
                <div class="text-sm font-semibold text-gray-900">$2.3B+ Value</div>
                <div class="text-xs text-gray-500">Client Generated</div>
              </div>
            </div>
          </div>
        </div>
      </div>
      
      <!-- Quote Section -->
      <div class="max-w-4xl mx-auto text-center">
        <div class="bg-gray-900 rounded-3xl p-12 text-white relative overflow-hidden">
          <div class="absolute inset-0 bg-gradient-to-r from-blue-600/20 to-purple-600/20"></div>
          <div class="relative z-10">
            <svg class="w-12 h-12 text-blue-400 mx-auto mb-6" fill="currentColor" viewBox="0 0 24 24">
              <path d="M6.5 10c-.223 0-.437.034-.65.065.069-.232.14-.468.254-.68.114-.308.292-.575.469-.844.148-.291.409-.488.601-.737.201-.242.475-.403.692-.604.213-.21.492-.315.714-.463.232-.133.434-.28.65-.35l.539-.222.474-.197-.485-1.938-.597.144c-.191.048-.424.104-.689.171-.271.05-.56.187-.882.312-.318.142-.686.238-1.028.466-.344.218-.741.4-1.091.692-.339.301-.748.562-1.05.945-.33.358-.656.734-.909 1.162-.293.408-.492.856-.702 1.299-.19.443-.343.896-.468 1.336-.237.882-.343 1.72-.384 2.437-.034.718-.014 1.315.028 1.747.015.204.043.402.063.539l.025.168.026-.006A4.5 4.5 0 1 0 6.5 10zm11 0c-.223 0-.437.034-.65.065.069-.232.14-.468.254-.68.114-.308.292-.575.469-.844.148-.291.409-.488.601-.737.201-.242.475-.403.692-.604.213-.21.492-.315.714-.463.232-.133.434-.28.65-.35l.539-.222.474-.197-.485-1.938-.597.144c-.191.048-.424.104-.689.171-.271.05-.56.187-.882.312-.318.142-.686.238-1.028.466-.344.218-.741.4-1.091.692-.339.301-.748.562-1.05.945-.33.358-.656.734-.909 1.162-.293.408-.492.856-.702 1.299-.19.443-.343.896-.468 1.336-.237.882-.343 1.72-.384 2.437-.034.718-.014 1.315.028 1.747.015.204.043.402.063.539l.025.168.026-.006A4.5 4.5 0 1 0 17.5 10z"/>
            </svg>
            <blockquote class="text-2xl md:text-3xl font-light mb-8 leading-relaxed">
              "Our mission has always been simple: to transform the way businesses leverage technology. 
              We don't just implement solutions – we architect the future."
            </blockquote>
            <div class="flex items-center justify-center space-x-4">
              <div class="w-12 h-12 bg-gradient-to-r from-blue-600 to-purple-600 rounded-full flex items-center justify-center">
                <span class="text-white font-bold">MB</span>
              </div>
              <div class="text-left">
                <div class="font-semibold">Michael Brown</div>
                <div class="text-blue-300 text-sm">CEO & Founder</div>
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
    
    // Animate story content
    gsap.fromTo('.story-content',
      { opacity: 0, x: -50 },
      {
        opacity: 1,
        x: 0,
        duration: 1,
        ease: 'power3.out',
        scrollTrigger: {
          trigger: '.story-content',
          start: 'top 80%',
          toggleActions: 'play none none reverse'
        }
      }
    )
    
    // Animate visual side
    gsap.fromTo('.story-visual',
      { opacity: 0, x: 50 },
      {
        opacity: 1,
        x: 0,
        duration: 1,
        ease: 'power3.out',
        scrollTrigger: {
          trigger: '.story-visual',
          start: 'top 80%',
          toggleActions: 'play none none reverse'
        }
      }
    )
    
    // Animate milestone items
    gsap.fromTo('.milestone-item',
      { opacity: 0, y: 30 },
      {
        opacity: 1,
        y: 0,
        duration: 0.6,
        stagger: 0.15,
        ease: 'back.out(1.7)',
        scrollTrigger: {
          trigger: '.milestone-item',
          start: 'top 85%',
          toggleActions: 'play none none reverse'
        }
      }
    )
    
    // Animate floating achievement cards
    gsap.to('.achievement-float:nth-child(2)', { y: -10, duration: 3, yoyo: true, repeat: -1, ease: 'sine.inOut' })
    gsap.to('.achievement-float:nth-child(3)', { y: -15, duration: 4, yoyo: true, repeat: -1, ease: 'sine.inOut', delay: 1 })
    
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