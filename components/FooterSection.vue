<template>
  <footer class="bg-gray-950 text-white relative overflow-hidden">
    <!-- Background Pattern -->
    <div class="absolute inset-0 opacity-5">
      <div class="absolute inset-0" style="background-image: radial-gradient(circle at 20% 80%, rgba(59, 130, 246, 0.1) 0%, transparent 50%), radial-gradient(circle at 80% 20%, rgba(147, 51, 234, 0.1) 0%, transparent 50%);"></div>
    </div>

    <!-- Floating Elements -->
    <div class="absolute inset-0 opacity-10">
      <div class="footer-float footer-float-1"></div>
      <div class="footer-float footer-float-2"></div>
      <div class="footer-float footer-float-3"></div>
    </div>

    <div class="container-custom py-20 relative z-10">
      <div class="grid lg:grid-cols-6 gap-12">
        <!-- Company Info - Enhanced -->
        <div class="lg:col-span-2">
          <div class="flex items-center space-x-3 mb-8">
            <span class="text-2xl font-bold font-heading">The qexle</span>
          </div>
          
          <p class="text-gray-300 mb-8 text-lg leading-relaxed">
            We architect, build, and deploy scalable technology solutions that transform how enterprises operate. From cloud migration to AI integration, we deliver measurable business outcomes with enterprise-grade excellence.
          </p>
          
          <!-- Company Deck Download -->
          <div class="mb-8">
            <button class="inline-flex items-center bg-lime-400 text-gray-900 px-6 py-3 rounded-full font-semibold hover:bg-lime-300 transition-all duration-300 transform hover:scale-105 shadow-lg">
              <span>Solutions Overview</span>
              <div class="ml-3 w-8 h-8 bg-gray-900 rounded-full flex items-center justify-center">
                <svg class="w-4 h-4 text-lime-400" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 14l-7 7m0 0l-7-7m7 7V3"></path>
                </svg>
              </div>
            </button>
          </div>
          
          <!-- Social Links -->
          <div class="flex space-x-4">
            <a href="#" class="text-gray-400 hover:text-white transition-colors duration-300 text-lg">LinkedIn</a>
            <a href="#" class="text-gray-400 hover:text-white transition-colors duration-300 text-lg">Twitter</a>
            <a href="#" class="text-gray-400 hover:text-white transition-colors duration-300 text-lg">GitHub</a>
            <a href="#" class="text-gray-400 hover:text-white transition-colors duration-300 text-lg">YouTube</a>
          </div>
        </div>
        
        <!-- Services Column 1 -->
        <div class="lg:col-span-1">
          <div class="space-y-6">
            <div class="service-link group cursor-pointer">
              <span class="text-gray-300 group-hover:text-white transition-colors duration-300 text-lg">Digital Transformation</span>
            </div>
            <div class="service-link group cursor-pointer">
              <span class="text-gray-300 group-hover:text-white transition-colors duration-300 text-lg">Cloud Solutions</span>
            </div>
            <div class="service-link group cursor-pointer">
              <span class="text-gray-300 group-hover:text-white transition-colors duration-300 text-lg">AI & Machine Learning</span>
            </div>
            <div class="service-link group cursor-pointer">
              <span class="text-gray-300 group-hover:text-white transition-colors duration-300 text-lg">Cybersecurity</span>
            </div>
            <div class="service-link group cursor-pointer">
              <span class="text-gray-300 group-hover:text-white transition-colors duration-300 text-lg">Mobile Development</span>
            </div>
          </div>
        </div>

        <!-- Services Column 2 -->
        <div class="lg:col-span-1">
          <div class="space-y-6">
            <div class="service-link group cursor-pointer">
              <span class="text-gray-300 group-hover:text-white transition-colors duration-300 text-lg">Performance Optimization</span>
            </div>
            <div class="service-link group cursor-pointer">
              <span class="text-gray-300 group-hover:text-white transition-colors duration-300 text-lg">Enterprise Architecture</span>
            </div>
            <div class="service-link group cursor-pointer">
              <span class="text-gray-300 group-hover:text-white transition-colors duration-300 text-lg">System Integration</span>
            </div>
            <div class="service-link group cursor-pointer">
              <span class="text-gray-300 group-hover:text-white transition-colors duration-300 text-lg">24/7 IT Support</span>
            </div>
          </div>
        </div>

        <!-- Industries Column 1 -->
        <div class="lg:col-span-1">
          <div class="space-y-6">
            <div class="portfolio-link group cursor-pointer">
              <span class="text-gray-300 group-hover:text-white transition-colors duration-300 text-lg">Manufacturing</span>
            </div>
            <div class="portfolio-link group cursor-pointer">
              <span class="text-gray-300 group-hover:text-white transition-colors duration-300 text-lg">Healthcare</span>
            </div>
            <div class="portfolio-link group cursor-pointer">
              <span class="text-gray-300 group-hover:text-white transition-colors duration-300 text-lg">Financial Services</span>
            </div>
            <div class="portfolio-link group cursor-pointer">
              <span class="text-gray-300 group-hover:text-white transition-colors duration-300 text-lg font-semibold">View all industries</span>
            </div>
          </div>
        </div>

        <!-- Resources Column -->
        <div class="lg:col-span-1">
          <div class="space-y-6">
            <div class="portfolio-link group cursor-pointer">
              <span class="text-gray-300 group-hover:text-white transition-colors duration-300 text-lg">Case Studies</span>
            </div>
            <div class="portfolio-link group cursor-pointer">
              <span class="text-gray-300 group-hover:text-white transition-colors duration-300 text-lg">Tech Blog</span>
            </div>
            <div class="portfolio-link group cursor-pointer">
              <span class="text-gray-300 group-hover:text-white transition-colors duration-300 text-lg">Documentation</span>
            </div>
            <div class="portfolio-link group cursor-pointer">
              <span class="text-gray-300 group-hover:text-white transition-colors duration-300 text-lg">Support Center</span>
            </div>
          </div>
        </div>
      </div>

      <!-- Call to Action Section -->
      <div class="mt-20 flex flex-col lg:flex-row items-start lg:items-center justify-between">
        <div class="mb-8 lg:mb-0">
          <p class="text-gray-400 text-lg mb-2">Ready to transform your business?</p>
          <h3 class="text-4xl md:text-5xl font-bold text-lime-400 font-heading">Let's build together</h3>
        </div>
        
        <div class="flex items-center">
          <button class="inline-flex items-center bg-lime-400 text-gray-900 px-8 py-4 rounded-full font-semibold text-lg hover:bg-lime-300 transition-all duration-300 transform hover:scale-105 shadow-lg group">
            <span>Start Your Project</span>
            <div class="ml-3 w-8 h-8 bg-gray-900 rounded-full flex items-center justify-center group-hover:rotate-45 transition-transform duration-300">
              <svg class="w-4 h-4 text-lime-400" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M7 17L17 7M17 7H7M17 7V17"></path>
              </svg>
            </div>
          </button>
        </div>
      </div>

      <!-- Bottom Section -->
      <div class="mt-16 pt-8 border-t border-gray-800">
        <div class="flex flex-col lg:flex-row items-start lg:items-center justify-between">
          <div class="mb-6 lg:mb-0">
            <p class="text-gray-400 text-sm">
              The qexle © 2025 - Enterprise Digital Transformation Solutions
            </p>
          </div>
          
          <div class="flex items-center space-x-6">
            <div class="text-gray-400 text-sm">
              <span class="font-semibold text-white">500+</span> Projects Delivered
            </div>
            <div class="text-gray-400 text-sm">
              <span class="font-semibold text-white">98%</span> Client Satisfaction
            </div>
            <div class="text-gray-400 text-sm">
              <span class="font-semibold text-white">$2.3B+</span> Client Value Generated
            </div>
          </div>
        </div>
      </div>
    </div>

    <!-- Bottom Brand Section -->
    <div class="bg-gray-950 py-0  overflow-hidden">
      <div class="w-full relative">
        <div class="text-center overflow-hidden">
          <h4 class="text-[4rem] md:text-[8rem] lg:text-[10rem] xl:text-[12rem] font-black text-white/5 font-heading tracking-[0.2em] leading-none select-none whitespace-nowrap transform translate-y-1/2">
            THE QEXLE
          </h4>
        </div>
      </div>
    </div>
  </footer>
</template>

<script setup>
import { onMounted } from 'vue'
import { gsap } from 'gsap'
import { ScrollTrigger } from 'gsap/ScrollTrigger'

onMounted(() => {
  if (process.client) {
    gsap.registerPlugin(ScrollTrigger)
    
    // Animate service links
    gsap.fromTo('.service-link',
      { opacity: 0, x: -20 },
      {
        opacity: 1,
        x: 0,
        duration: 0.6,
        stagger: 0.1,
        ease: 'power3.out',
        scrollTrigger: {
          trigger: '.service-link',
          start: 'top 90%',
          toggleActions: 'play none none reverse'
        }
      }
    )
    
    // Animate portfolio links
    gsap.fromTo('.portfolio-link',
      { opacity: 0, x: 20 },
      {
        opacity: 1,
        x: 0,
        duration: 0.6,
        stagger: 0.1,
        ease: 'power3.out',
        scrollTrigger: {
          trigger: '.portfolio-link',
          start: 'top 90%',
          toggleActions: 'play none none reverse'
        }
      }
    )

    // Animate floating elements
    gsap.to('.footer-float-1', { y: -15, duration: 4, yoyo: true, repeat: -1, ease: 'sine.inOut' })
    gsap.to('.footer-float-2', { y: -20, duration: 3.5, yoyo: true, repeat: -1, ease: 'sine.inOut', delay: 1 })
    gsap.to('.footer-float-3', { y: -12, duration: 4.5, yoyo: true, repeat: -1, ease: 'sine.inOut', delay: 2 })
  }
})
</script>

<style scoped>
.footer-float {
  position: absolute;
  width: 8px;
  height: 8px;
  background: linear-gradient(45deg, #3b82f6, #8b5cf6);
  border-radius: 50%;
  opacity: 0.4;
}

.footer-float-1 { top: 20%; left: 10%; }
.footer-float-2 { top: 60%; right: 15%; }
.footer-float-3 { bottom: 30%; left: 25%; }
</style>