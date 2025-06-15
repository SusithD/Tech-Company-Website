<template>
  <section id="contact" class="section-padding bg-white">
    <div class="container-custom">
      <div class="text-center mb-16">
        <h2 class="text-4xl md:text-5xl font-bold mb-6 text-gray-900">
          Contact Us
        </h2>
        <p class="text-xl text-gray-600">Get in touch to start your digital transformation journey</p>
      </div>
      
      <div class="grid lg:grid-cols-2 gap-12">
        <!-- Contact Info -->
        <div class="contact-info space-y-8">
          <div class="bg-gray-50 p-8 rounded-2xl border border-gray-100">
            <h3 class="text-xl font-bold mb-6 text-gray-900">Get in Touch</h3>
            <div class="space-y-4">
              <div class="flex items-center space-x-4">
                <div class="w-10 h-10 bg-gray-900 rounded-full flex items-center justify-center">
                  <span class="text-white text-sm">📧</span>
                </div>
                <span class="text-gray-600">support@mbtech.com</span>
              </div>
              <div class="flex items-center space-x-4">
                <div class="w-10 h-10 bg-gray-900 rounded-full flex items-center justify-center">
                  <span class="text-white text-sm">📞</span>
                </div>
                <span class="text-gray-600">+123-456-7890</span>
              </div>
            </div>
          </div>
          
          <div class="bg-gray-50 p-8 rounded-2xl border border-gray-100">
            <h3 class="text-xl font-bold mb-6 text-gray-900">Offices</h3>
            <div class="space-y-6">
              <div>
                <h4 class="font-semibold text-gray-900 mb-2">United States</h4>
                <p class="text-gray-600 text-sm">
                  8333 Bryan Dairy Rd,<br>
                  Seminole, FL 33777, US
                </p>
              </div>
              <div>
                <h4 class="font-semibold text-gray-900 mb-2">Sri Lanka</h4>
                <p class="text-gray-600 text-sm">
                  Level 12, One Galle Face Tower,<br>
                  Centre Road, Colombo 02, Sri Lanka
                </p>
              </div>
            </div>
          </div>
        </div>
        
        <!-- Contact Form -->
        <div class="contact-form">
          <form @submit.prevent="submitForm" class="bg-gray-50 p-8 rounded-2xl border border-gray-100 space-y-6">
            <div>
              <label for="name" class="block text-sm font-medium text-gray-700 mb-2">Name *</label>
              <input
                type="text"
                id="name"
                v-model="form.name"
                required
                class="w-full px-4 py-3 bg-white border border-gray-200 rounded-lg text-gray-900 placeholder-gray-500 focus:outline-none focus:ring-2 focus:ring-gray-900 focus:border-transparent transition-all"
                placeholder="Your full name"
              >
            </div>
            
            <div>
              <label for="email" class="block text-sm font-medium text-gray-700 mb-2">Email *</label>
              <input
                type="email"
                id="email"
                v-model="form.email"
                required
                class="w-full px-4 py-3 bg-white border border-gray-200 rounded-lg text-gray-900 placeholder-gray-500 focus:outline-none focus:ring-2 focus:ring-gray-900 focus:border-transparent transition-all"
                placeholder="your@email.com"
              >
            </div>
            
            <div>
              <label for="message" class="block text-sm font-medium text-gray-700 mb-2">Message</label>
              <textarea
                id="message"
                v-model="form.message"
                rows="4"
                class="w-full px-4 py-3 bg-white border border-gray-200 rounded-lg text-gray-900 placeholder-gray-500 focus:outline-none focus:ring-2 focus:ring-gray-900 focus:border-transparent transition-all resize-none"
                placeholder="Tell us about your project..."
              ></textarea>
            </div>
            
            <button type="submit" class="btn-primary w-full text-lg">
              Send Message
            </button>
          </form>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
import { reactive, onMounted } from 'vue'
import { gsap } from 'gsap'
import { ScrollTrigger } from 'gsap/ScrollTrigger'

const form = reactive({
  name: '',
  email: '',
  message: ''
})

const submitForm = () => {
  console.log('Form submitted:', form)
}

onMounted(() => {
  if (process.client) {
    gsap.registerPlugin(ScrollTrigger)
    
    gsap.fromTo('.contact-info',
      { opacity: 0, x: -30 },
      {
        opacity: 1,
        x: 0,
        duration: 0.8,
        ease: 'power3.out',
        scrollTrigger: {
          trigger: '.contact-info',
          start: 'top 80%',
          toggleActions: 'play none none reverse'
        }
      }
    )
    
    gsap.fromTo('.contact-form',
      { opacity: 0, x: 30 },
      {
        opacity: 1,
        x: 0,
        duration: 0.8,
        ease: 'power3.out',
        scrollTrigger: {
          trigger: '.contact-form',
          start: 'top 80%',
          toggleActions: 'play none none reverse'
        }
      }
    )
  }
})
</script>