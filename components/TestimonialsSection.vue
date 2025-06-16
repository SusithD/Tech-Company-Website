<template>
  <section class="section-padding bg-gradient-to-br from-white via-gray-50 to-white relative overflow-hidden">
    <!-- Background Pattern -->
    <div class="absolute inset-0 opacity-5">
      <div class="absolute inset-0" style="background-image: radial-gradient(circle at 20% 60%, rgba(59, 130, 246, 0.1) 0%, transparent 50%), radial-gradient(circle at 80% 40%, rgba(147, 51, 234, 0.1) 0%, transparent 50%);"></div>
    </div>

    <div class="container-custom relative z-10">
      <!-- Enhanced Header with Big Typography -->
      <div class="max-w-6xl mx-auto text-center mb-20">
        <div class="inline-flex items-center bg-green-100 text-green-800 px-6 py-3 rounded-full text-sm font-semibold mb-8 animate-pulse">
          <span class="w-2 h-2 bg-green-500 rounded-full mr-3"></span>
          CLIENT SUCCESS STORIES
        </div>
        
        <h2 class="text-6xl md:text-7xl lg:text-8xl font-bold mb-8 text-gray-900 font-heading leading-tight">
          What Our
          <span class="block gradient-text animate-gradient">Clients Say</span>
        </h2>
        
        <p class="text-2xl md:text-3xl text-gray-600 leading-relaxed max-w-4xl mx-auto font-light">
          Don't just take our word for it. Here's what <span class="font-semibold text-gray-800">enterprise leaders</span> 
          say about working with us and achieving 
          <span class="font-semibold gradient-text">transformational results</span>.
        </p>
      </div>

      <!-- Interactive Testimonials Grid -->
      <div class="grid md:grid-cols-2 lg:grid-cols-3 gap-8 mb-20">
        <div v-for="(testimonial, index) in testimonials" :key="testimonial.name" 
             class="testimonial-card group relative bg-white p-8 rounded-3xl border border-gray-200 hover:border-blue-300 transition-all duration-500 cursor-pointer overflow-hidden"
             @mouseenter="handleTestimonialHover(index, true)"
             @mouseleave="handleTestimonialHover(index, false)">
          
          <!-- Card Background Animation -->
          <div class="absolute inset-0 bg-gradient-to-br from-blue-50 to-green-50 opacity-0 group-hover:opacity-100 transition-opacity duration-500"></div>
          
          <div class="relative z-10">
            <!-- Interactive Stars -->
            <div class="flex items-center space-x-1 mb-6">
              <div class="flex text-yellow-400 group-hover:text-yellow-500 transition-colors duration-300">
                <StarIcon v-for="i in 5" :key="i" class="w-5 h-5 fill-current transform group-hover:scale-110 transition-transform duration-300" :style="`transition-delay: ${i * 50}ms`" />
              </div>
              <span class="text-sm text-gray-500 ml-2 opacity-0 group-hover:opacity-100 transition-opacity duration-500">{{ testimonial.rating }}/5</span>
            </div>

            <!-- Quote -->
            <div class="text-4xl text-gray-300 mb-4 group-hover:text-blue-400 transition-colors duration-300">"</div>
            <blockquote class="text-gray-700 leading-relaxed mb-8 group-hover:text-gray-800 transition-colors duration-300 text-lg">
              {{ testimonial.quote }}
            </blockquote>

            <!-- Profile -->
            <div class="flex items-center space-x-4">
              <div class="relative">
                <div :class="testimonial.avatarClass" class="w-14 h-14 rounded-full flex items-center justify-center group-hover:scale-110 transition-transform duration-300">
                  <span class="text-white font-bold">{{ testimonial.initials }}</span>
                </div>
                <!-- Success Badge -->
                <div class="absolute -top-1 -right-1 w-5 h-5 bg-green-500 rounded-full opacity-0 group-hover:opacity-100 transition-opacity duration-500 flex items-center justify-center">
                  <CheckIcon class="w-3 h-3 text-white" />
                </div>
              </div>
              <div>
                <div class="text-gray-900 font-bold text-lg group-hover:text-blue-900 transition-colors duration-300">{{ testimonial.name }}</div>
                <div class="text-gray-600 text-sm group-hover:text-blue-600 transition-colors duration-300">{{ testimonial.position }}</div>
                <div class="text-xs text-gray-400 group-hover:text-blue-500 transition-colors duration-300">{{ testimonial.company }}</div>
              </div>
            </div>

            <!-- Impact Metric -->
            <div class="mt-6 p-4 bg-gray-50 rounded-2xl group-hover:bg-white transition-colors duration-300">
              <div class="text-2xl font-bold text-green-600 mb-1">{{ testimonial.impact }}</div>
              <div class="text-xs text-gray-500">{{ testimonial.impactDesc }}</div>
            </div>
          </div>
        </div>
      </div>

      <!-- FAQ Section (Inspired by your screenshot) -->
      <div class="max-w-4xl mx-auto mb-20">
        <div class="text-center mb-16">
          <h3 class="text-4xl md:text-5xl font-bold mb-6 text-gray-900 font-heading">
            Frequently Asked Questions
          </h3>
          <p class="text-xl text-gray-600">
            Everything you need to know about working with us
          </p>
        </div>

        <div class="space-y-4">
          <div v-for="(faq, index) in faqs" :key="faq.question"
               class="faq-item group bg-white border border-gray-200 rounded-2xl overflow-hidden hover:border-blue-300 transition-all duration-300">
            <button 
              @click="toggleFAQ(index)"
              class="w-full p-8 text-left flex items-center justify-between hover:bg-gray-50 transition-colors duration-300">
              <span class="text-lg font-semibold text-gray-900 group-hover:text-blue-900 transition-colors duration-300">{{ faq.question }}</span>
              <div class="w-8 h-8 bg-gray-100 rounded-full flex items-center justify-center group-hover:bg-blue-100 transition-all duration-300" 
                   :class="{ 'rotate-45': faq.isOpen }">
                <span class="text-gray-600 group-hover:text-blue-600 text-xl transition-colors duration-300">{{ faq.isOpen ? '×' : '↗' }}</span>
              </div>
            </button>
            <div v-show="faq.isOpen" class="px-8 pb-8">
              <p class="text-gray-600 leading-relaxed">{{ faq.answer }}</p>
            </div>
          </div>
        </div>
      </div>
      <!-- Enhanced CTA Section -->
      <div class="bg-gray-900 rounded-3xl p-12 text-center text-white relative overflow-hidden">
        <div class="absolute inset-0 bg-gradient-to-r from-blue-600/20 to-green-600/20 animate-pulse"></div>
        
        <div class="relative z-10">
          <h3 class="text-4xl md:text-5xl font-bold mb-6 font-heading">
            Ready to Join Them?
          </h3>
          <p class="text-xl text-gray-300 mb-8 max-w-2xl mx-auto">
            Join 500+ companies that have already transformed their business with our solutions.
          </p>
          
          <div class="flex flex-col sm:flex-row items-center justify-center gap-6">
            <button class="bg-white text-gray-900 px-8 py-4 rounded-full font-semibold hover:bg-gray-100 transition-all duration-300 transform hover:scale-105">
              Start Your Project →
            </button>
            <button class="border-2 border-white text-white px-8 py-4 rounded-full font-semibold hover:bg-white hover:text-gray-900 transition-all duration-300">
              View All Testimonials
            </button>
          </div>

          <!-- Trust Indicators -->
          <div class="flex flex-col md:flex-row items-center justify-center space-y-4 md:space-y-0 md:space-x-12 mt-12 text-gray-300">
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
    </div>
  </section>
</template>

<script setup>
import { onMounted, ref } from 'vue'
import { gsap } from 'gsap'
import { ScrollTrigger } from 'gsap/ScrollTrigger'
import { StarIcon, CheckIcon } from '@heroicons/vue/24/solid'
import { ChatBubbleLeftRightIcon } from '@heroicons/vue/24/outline'

const testimonials = [
  {
    name: 'Rachel Kim',
    position: 'VP Technology',
    company: 'Innovent Health',
    initials: 'RK',
    avatarClass: 'bg-gradient-to-r from-blue-600 to-purple-600',
    quote: 'MB Tech transformed our entire digital infrastructure. Their expertise in enterprise solutions is unmatched, and the results speak for themselves.',
    rating: '5.0',
    impact: '+400%',
    impactDesc: 'System Performance'
  },
  {
    name: 'Michael Chen',
    position: 'CTO',
    company: 'DataFlow Solutions',
    initials: 'MC',
    avatarClass: 'bg-gradient-to-r from-purple-600 to-blue-800',
    quote: 'Outstanding technical depth and project management. They delivered a complex system integration ahead of schedule and under budget.',
    rating: '5.0',
    impact: '+250%',
    impactDesc: 'Development Speed'
  },
  {
    name: 'Sarah Patel',
    position: 'Director of IT',
    company: 'GlobalTech',
    initials: 'SP',
    avatarClass: 'bg-gradient-to-r from-blue-800 to-green-600',
    quote: 'Their team became an extension of ours. The level of collaboration and expertise they brought to our digital transformation was exceptional.',
    rating: '5.0',
    impact: '+300%',
    impactDesc: 'Operational Efficiency'
  }
]

const faqs = ref([
  {
    question: 'What are your focus areas as a tech solutions company?',
    answer: 'We specialize in enterprise-grade digital transformation, cloud migration, AI integration, cybersecurity, and custom software development. Our focus is on scalable solutions that drive measurable business outcomes.',
    isOpen: false
  },
  {
    question: 'Why is digital transformation important for business growth?',
    answer: 'Digital transformation enables businesses to operate more efficiently, reach new markets, improve customer experiences, and stay competitive. Our solutions typically result in 200-400% improvement in operational efficiency.',
    isOpen: false
  },
  {
    question: 'My business isn\'t generating enough leads. How can your solutions help?',
    answer: 'We develop comprehensive digital strategies including modern web applications, mobile solutions, and data analytics platforms that improve customer engagement and conversion rates by an average of 300%.',
    isOpen: false
  },
  {
    question: 'What separates us from other top tech solution providers?',
    answer: 'Our unique combination of enterprise expertise, agile methodology, 24/7 support, and proven track record of 98% client satisfaction. We become your strategic tech partner, not just a service provider.',
    isOpen: false
  },
  {
    question: 'How could you help us modernize our app, website, or enterprise software?',
    answer: 'We provide end-to-end modernization services including UX/UI redesign, cloud migration, performance optimization, and integration of modern technologies like AI and machine learning.',
    isOpen: false
  },
  {
    question: 'Do you work with startups or only with enterprise companies?',
    answer: 'We work with both! From innovative startups to Fortune 500 enterprises. Our scalable approach ensures we deliver the right solution regardless of company size, with pricing models that fit every budget.',
    isOpen: false
  }
])

const toggleFAQ = (index) => {
  faqs.value[index].isOpen = !faqs.value[index].isOpen
}

const handleTestimonialHover = (index, isHover) => {
  if (process.client) {
    const card = document.querySelectorAll('.testimonial-card')[index]
    if (isHover) {
      gsap.to(card, {
        y: -10,
        scale: 1.02,
        duration: 0.3,
        ease: 'power2.out'
      })
    } else {
      gsap.to(card, {
        y: 0,
        scale: 1,
        duration: 0.3,
        ease: 'power2.out'
      })
    }
  }
}

onMounted(() => {
  if (process.client) {
    gsap.registerPlugin(ScrollTrigger)
    
    // Animate gradient text
    gsap.fromTo('.gradient-text',
      { backgroundPosition: '200% center' },
      {
        backgroundPosition: '-200% center',
        duration: 4,
        ease: 'none',
        repeat: -1
      }
    )
    
    // Animate testimonial cards
    gsap.fromTo('.testimonial-card',
      { opacity: 0, y: 50, scale: 0.9 },
      {
        opacity: 1,
        y: 0,
        scale: 1,
        duration: 0.8,
        stagger: 0.15,
        ease: 'back.out(1.7)',
        scrollTrigger: {
          trigger: '.testimonial-card',
          start: 'top 85%',
          toggleActions: 'play none none reverse'
        }
      }
    )

    // Animate FAQ items
    gsap.fromTo('.faq-item',
      { opacity: 0, x: -30 },
      {
        opacity: 1,
        x: 0,
        duration: 0.6,
        stagger: 0.1,
        ease: 'power3.out',
        scrollTrigger: {
          trigger: '.faq-item',
          start: 'top 85%',
          toggleActions: 'play none none reverse'
        }
      }
    )
  }
})
</script>

<style scoped>
.animate-gradient {
  background: linear-gradient(270deg, #3b82f6, #10b981, #3b82f6);
  background-size: 400% 400%;
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  background-clip: text;
}
</style>