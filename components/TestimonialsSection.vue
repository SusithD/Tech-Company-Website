<template>
  <section class="section-padding bg-gray-50">
    <div class="container-custom">
      <!-- Header -->
      <div class="text-center mb-16">
        <h2 class="text-4xl md:text-5xl font-bold mb-6 text-gray-900">
          What Our Clients Say
        </h2>
        <p class="text-xl text-gray-600 max-w-3xl mx-auto">
          Don't just take our word for it. Here's what enterprise leaders say about working with us.
        </p>
      </div>
      
      <!-- Testimonials Grid -->
      <div class="grid md:grid-cols-2 lg:grid-cols-3 gap-8 mb-16">
        <!-- Testimonial 1 -->
        <div class="testimonial-card bg-white p-8 rounded-2xl border border-gray-200 card-hover">
          <div class="flex items-center space-x-1 mb-6">
            <div class="flex text-yellow-400">
              <StarIcon v-for="i in 5" :key="i" class="w-4 h-4 fill-current" />
            </div>
          </div>
          <blockquote class="text-gray-700 leading-relaxed mb-6">
            "MB Tech transformed our entire digital infrastructure. Their expertise in enterprise solutions is unmatched, and the results speak for themselves."
          </blockquote>
          <div class="flex items-center space-x-4">
            <div class="w-12 h-12 bg-gradient-to-r from-blue-600 to-purple-600 rounded-full flex items-center justify-center">
              <span class="text-white font-bold text-sm">RK</span>
            </div>
            <div>
              <div class="text-gray-900 font-semibold">Rachel Kim</div>
              <div class="text-gray-600 text-sm">VP Technology, Innovent Health</div>
            </div>
          </div>
        </div>

        <!-- Testimonial 2 -->
        <div class="testimonial-card bg-white p-8 rounded-2xl border border-gray-200 card-hover">
          <div class="flex items-center space-x-1 mb-6">
            <div class="flex text-yellow-400">
              <StarIcon v-for="i in 5" :key="i" class="w-4 h-4 fill-current" />
            </div>
          </div>
          <blockquote class="text-gray-700 leading-relaxed mb-6">
            "Outstanding technical depth and project management. They delivered a complex system integration ahead of schedule and under budget."
          </blockquote>
          <div class="flex items-center space-x-4">
            <div class="w-12 h-12 bg-gradient-to-r from-purple-600 to-blue-800 rounded-full flex items-center justify-center">
              <span class="text-white font-bold text-sm">MC</span>
            </div>
            <div>
              <div class="text-gray-900 font-semibold">Michael Chen</div>
              <div class="text-gray-600 text-sm">CTO, DataFlow Solutions</div>
            </div>
          </div>
        </div>

        <!-- Testimonial 3 -->
        <div class="testimonial-card bg-white p-8 rounded-2xl border border-gray-200 card-hover md:col-span-2 lg:col-span-1">
          <div class="flex items-center space-x-1 mb-6">
            <div class="flex text-yellow-400">
              <StarIcon v-for="i in 5" :key="i" class="w-4 h-4 fill-current" />
            </div>
          </div>
          <blockquote class="text-gray-700 leading-relaxed mb-6">
            "Their team became an extension of ours. The level of collaboration and expertise they brought to our digital transformation was exceptional."
          </blockquote>
          <div class="flex items-center space-x-4">
            <div class="w-12 h-12 bg-gradient-to-r from-blue-800 to-blue-600 rounded-full flex items-center justify-center">
              <span class="text-white font-bold text-sm">SP</span>
            </div>
            <div>
              <div class="text-gray-900 font-semibold">Sarah Patel</div>
              <div class="text-gray-600 text-sm">Director of IT, GlobalTech</div>
            </div>
          </div>
        </div>
      </div>

      <!-- Featured Testimonial -->
      <div class="max-w-4xl mx-auto">
        <div class="featured-testimonial bg-white p-8 md:p-12 rounded-2xl border border-gray-200 text-center card-hover">
          <div class="text-6xl mb-6 text-gray-300">"</div>
          <blockquote class="text-xl md:text-2xl text-gray-700 leading-relaxed mb-8 font-medium">
            From the very first call, MB Tech demonstrated professionalism and deep technical understanding. 
            They designed a user-centric solution that improved our efficiency by 300% and elevated our entire user experience. 
            Their attention to detail and commitment to quality were apparent in every phase.
          </blockquote>
          <div class="flex items-center justify-center space-x-4 mb-8">
            <div class="w-16 h-16 bg-gradient-to-r from-blue-600 via-purple-600 to-blue-800 rounded-full flex items-center justify-center">
              <span class="text-white font-bold text-lg">JD</span>
            </div>
            <div class="text-left">
              <div class="text-gray-900 font-bold text-lg">James Davidson</div>
              <div class="text-gray-600">CEO, Enterprise Solutions Inc.</div>
            </div>
          </div>
          <div class="flex items-center justify-center space-x-1">
            <div class="flex text-yellow-400">
              <StarIcon v-for="i in 5" :key="i" class="w-5 h-5 fill-current" />
            </div>
            <span class="text-gray-600 ml-3">Rated 5/5 across all projects</span>
          </div>
        </div>
      </div>
      
      <!-- Bottom CTA -->
      <div class="text-center mt-16">
        <div class="bg-gray-900 text-white p-8 md:p-12 rounded-2xl">
          <h3 class="text-2xl md:text-3xl font-bold mb-4">
            "No tech challenge is out of our orbit."
          </h3>
          <p class="text-gray-300 text-lg mb-6 max-w-2xl mx-auto">
            Ready to join our satisfied clients? Let's discuss how we can transform your business.
          </p>
          <button class="bg-white text-gray-900 px-8 py-3 rounded-full font-semibold transition-all duration-300 hover:bg-gray-100 hover:shadow-lg transform hover:-translate-y-0.5">
            Start Your Project →
          </button>
        </div>
      </div>

      <!-- Trust Indicators -->
      <div class="text-center mt-16">
        <div class="flex flex-col md:flex-row items-center justify-center space-y-4 md:space-y-0 md:space-x-12 text-gray-600">
          <div class="flex items-center space-x-2">
            <div class="w-6 h-6 bg-green-500 rounded-full flex items-center justify-center">
              <CheckIcon class="w-3 h-3 text-white" />
            </div>
            <span class="font-semibold">500+ Projects Delivered</span>
          </div>
          <div class="flex items-center space-x-2">
            <div class="w-6 h-6 bg-green-500 rounded-full flex items-center justify-center">
              <CheckIcon class="w-3 h-3 text-white" />
            </div>
            <span class="font-semibold">98% Client Satisfaction</span>
          </div>
          <div class="flex items-center space-x-2">
            <div class="w-6 h-6 bg-green-500 rounded-full flex items-center justify-center">
              <CheckIcon class="w-3 h-3 text-white" />
            </div>
            <span class="font-semibold">24/7 Support</span>
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
import { StarIcon, CheckIcon } from '@heroicons/vue/24/solid'

onMounted(() => {
  if (process.client) {
    gsap.registerPlugin(ScrollTrigger)
    
    // Animate testimonial cards
    gsap.fromTo('.testimonial-card',
      { opacity: 0, y: 30 },
      {
        opacity: 1,
        y: 0,
        duration: 0.8,
        stagger: 0.2,
        ease: 'power3.out',
        scrollTrigger: {
          trigger: '.testimonial-card',
          start: 'top 85%',
          toggleActions: 'play none none reverse'
        }
      }
    )

    // Animate featured testimonial
    gsap.fromTo('.featured-testimonial',
      { opacity: 0, scale: 0.95 },
      {
        opacity: 1,
        scale: 1,
        duration: 0.8,
        ease: 'power3.out',
        scrollTrigger: {
          trigger: '.featured-testimonial',
          start: 'top 80%',
          toggleActions: 'play none none reverse'
        }
      }
    )
  }
})
</script>