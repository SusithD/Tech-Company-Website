<template>
  <section class="section-padding bg-white">
    <div class="container-custom">
      <div class="text-center mb-16">
        <h2 class="text-4xl md:text-5xl font-bold mb-6 text-gray-900">
          Testimonials
        </h2>
        <p class="text-xl text-gray-600">What our clients say about us</p>
      </div>
      
      <div class="max-w-4xl mx-auto">
        <div class="testimonial-card bg-gray-50 p-8 md:p-12 rounded-2xl border border-gray-100 text-center">
          <div class="text-6xl mb-6 text-gray-300">"</div>
          <blockquote class="text-lg md:text-xl text-gray-700 leading-relaxed mb-8">
            From the very first call, MB Tech demonstrated professionalism and deep technical understanding. 
            They designed a user-centric solution that improved our efficiency and elevated the user experience. 
            Their attention to detail and commitment to quality were apparent in every phase. 
            We look forward to continuing this relationship.
          </blockquote>
          <div class="flex items-center justify-center space-x-4">
            <div class="w-12 h-12 bg-gray-900 rounded-full flex items-center justify-center">
              <span class="text-white font-bold">RK</span>
            </div>
            <div class="text-left">
              <div class="text-gray-900 font-semibold">Rachel Kim</div>
              <div class="text-gray-600">VP of Technology, Innovent Health</div>
            </div>
          </div>
        </div>
      </div>
      
      <div class="text-center mt-16">
        <p class="text-2xl md:text-3xl font-bold text-gray-900 mb-4">
          "No tech challenge is out of our orbit."
        </p>
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
    
    gsap.fromTo('.testimonial-card',
      { opacity: 0, scale: 0.95 },
      {
        opacity: 1,
        scale: 1,
        duration: 0.8,
        ease: 'power3.out',
        scrollTrigger: {
          trigger: '.testimonial-card',
          start: 'top 80%',
          toggleActions: 'play none none reverse'
        }
      }
    )
  }
})
</script>