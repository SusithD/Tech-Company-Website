<template>
  <section class="section-padding bg-gray-50">
    <div class="container-custom">
      <div class="text-center mb-16">
        <h2 class="text-4xl md:text-5xl font-bold mb-6 text-gray-900">
          Why Choose Us
        </h2>
        <p class="text-xl text-gray-600 max-w-4xl mx-auto leading-relaxed">
          We drive exponential growth through cutting-edge technologies and scalable solutions 
          that adapt to change leveraging innovations to take your business beyond today's limits.
        </p>
      </div>
      
      <div class="grid lg:grid-cols-2 gap-8">
        <div v-for="feature in features" :key="feature.title" 
             class="feature-card bg-white p-8 rounded-2xl border border-gray-100 card-hover group">
          <div class="flex items-start space-x-6">
            <div class="flex-shrink-0">
              <div class="w-12 h-12 bg-gray-900 rounded-xl flex items-center justify-center text-white text-xl font-bold">
                {{ feature.icon }}
              </div>
            </div>
            <div class="flex-1">
              <h3 class="text-xl font-bold mb-3 text-gray-900">
                {{ feature.title }}
              </h3>
              <p class="text-gray-600 leading-relaxed">
                {{ feature.description }}
              </p>
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

const features = [
  {
    icon: '🤝',
    title: 'Strategic Tech Partnership',
    description: 'We don\'t just deliver services we become your tech partner, aligning our expertise with your goals to drive real impact.'
  },
  {
    icon: '🔄',
    title: 'Scalable Innovation',
    description: 'We harness emerging technologies to enable you to disrupt your industry and grow without limits.'
  },
  {
    icon: '⚡',
    title: 'Optimised IT Efficiency',
    description: 'We focus on performance, reliability, and results ensuring your IT works smarter, faster, and better.'
  },
  {
    icon: '🚀',
    title: 'Agile & Reliable Deployment',
    description: 'We ensure rapid, reliable deployments through an agile approach that minimizes downtime and safeguards business continuity.'
  },
  {
    icon: '🛡️',
    title: 'Proactive IT Continuity',
    description: 'We monitor your systems 24/7, solving issues before they arise and keeping your business running smoothly.'
  },
  {
    icon: '🎯',
    title: 'Results-Driven Approach',
    description: 'Every solution is designed with measurable outcomes in mind, ensuring maximum ROI and business impact.'
  }
]

onMounted(() => {
  if (process.client) {
    gsap.registerPlugin(ScrollTrigger)
    
    gsap.fromTo('.feature-card',
      { opacity: 0, y: 30 },
      {
        opacity: 1,
        y: 0,
        duration: 0.6,
        stagger: 0.1,
        ease: 'power3.out',
        scrollTrigger: {
          trigger: '.feature-card',
          start: 'top 85%',
          toggleActions: 'play none none reverse'
        }
      }
    )
  }
})
</script>