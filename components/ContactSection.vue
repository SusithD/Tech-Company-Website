<template>
  <section id="contact" class="section-padding bg-gradient-to-br from-gray-50 via-white to-gray-50 relative overflow-hidden">
    <!-- Background Pattern -->
    <div class="absolute inset-0 opacity-5">
      <div class="absolute inset-0" style="background-image: radial-gradient(circle at 25% 75%, rgba(59, 130, 246, 0.1) 0%, transparent 50%), radial-gradient(circle at 75% 25%, rgba(16, 185, 129, 0.1) 0%, transparent 50%);"></div>
    </div>

    <!-- Floating Elements -->
    <div class="absolute inset-0 opacity-10">
      <div class="contact-float contact-float-1"></div>
      <div class="contact-float contact-float-2"></div>
      <div class="contact-float contact-float-3"></div>
    </div>

    <div class="container-custom relative z-10">
      <!-- Enhanced Header with Big Typography -->
      <div class="max-w-6xl mx-auto text-center mb-20">
        <div class="inline-flex items-center bg-blue-100 text-blue-800 px-6 py-3 rounded-full text-sm font-semibold mb-8 animate-pulse">
          <span class="w-2 h-2 bg-blue-500 rounded-full mr-3"></span>
          LET'S BUILD TOGETHER
        </div>
        
        <h2 class="text-6xl md:text-7xl lg:text-8xl font-bold mb-8 text-gray-900 font-heading leading-tight">
          Ready to
          <span class="block gradient-text animate-gradient">Transform</span>
          <span class="block text-5xl md:text-6xl lg:text-7xl text-gray-700">Your Business?</span>
        </h2>
        
        <p class="text-2xl md:text-3xl text-gray-600 leading-relaxed max-w-4xl mx-auto font-light">
          Get in touch to start your <span class="font-semibold text-gray-800">digital transformation journey</span>. 
          Let's discuss how we can <span class="font-semibold gradient-text">accelerate your success</span>.
        </p>
      </div>
      
      <div class="grid lg:grid-cols-2 gap-16 items-start">
        <!-- Enhanced Contact Info -->
        <div class="contact-info space-y-8">
          <!-- Main Contact Card -->
          <div class="group bg-white p-10 rounded-3xl border border-gray-200 shadow-lg hover:shadow-xl transition-all duration-500 relative overflow-hidden">
            <div class="absolute inset-0 bg-gradient-to-br from-blue-50 to-green-50 opacity-0 group-hover:opacity-100 transition-opacity duration-500"></div>
            
            <div class="relative z-10">
              <div class="flex items-center space-x-4 mb-8">
                <div class="w-16 h-16 bg-gray-900 rounded-2xl flex items-center justify-center group-hover:scale-110 group-hover:bg-blue-900 transition-all duration-500">
                  <EnvelopeIcon class="w-8 h-8 text-white" />
                </div>
                <div>
                  <h3 class="text-2xl font-bold text-gray-900 group-hover:text-blue-900 transition-colors duration-300 font-heading">Get in Touch</h3>
                  <p class="text-gray-600 group-hover:text-blue-600 transition-colors duration-300">We're here to help you succeed</p>
                </div>
              </div>
              
              <div class="space-y-6">
                <div class="contact-item group/item flex items-center space-x-4 p-4 rounded-2xl hover:bg-gray-50 transition-all duration-300 cursor-pointer">
                  <div class="w-12 h-12 bg-blue-100 rounded-xl flex items-center justify-center group-hover/item:bg-blue-200 group-hover/item:scale-110 transition-all duration-300">
                    <EnvelopeIcon class="w-6 h-6 text-blue-600" />
                  </div>
                  <div>
                    <div class="font-semibold text-gray-900 group-hover/item:text-blue-900 transition-colors duration-300">Email Us</div>
                    <div class="text-gray-600 group-hover/item:text-blue-600 transition-colors duration-300">support@theqexle.com</div>
                  </div>
                  <div class="ml-auto opacity-0 group-hover/item:opacity-100 transition-opacity duration-300">
                    <ArrowTopRightOnSquareIcon class="w-5 h-5 text-blue-600" />
                  </div>
                </div>
                
                <div class="contact-item group/item flex items-center space-x-4 p-4 rounded-2xl hover:bg-gray-50 transition-all duration-300 cursor-pointer">
                  <div class="w-12 h-12 bg-green-100 rounded-xl flex items-center justify-center group-hover/item:bg-green-200 group-hover/item:scale-110 transition-all duration-300">
                    <PhoneIcon class="w-6 h-6 text-green-600" />
                  </div>
                  <div>
                    <div class="font-semibold text-gray-900 group-hover/item:text-green-900 transition-colors duration-300">Call Us</div>
                    <div class="text-gray-600 group-hover/item:text-green-600 transition-colors duration-300">+1 (555) 123-4567</div>
                  </div>
                  <div class="ml-auto opacity-0 group-hover/item:opacity-100 transition-opacity duration-300">
                    <ArrowTopRightOnSquareIcon class="w-5 h-5 text-green-600" />
                  </div>
                </div>

                <div class="contact-item group/item flex items-center space-x-4 p-4 rounded-2xl hover:bg-gray-50 transition-all duration-300 cursor-pointer">
                  <div class="w-12 h-12 bg-purple-100 rounded-xl flex items-center justify-center group-hover/item:bg-purple-200 group-hover/item:scale-110 transition-all duration-300">
                    <ChatBubbleLeftRightIcon class="w-6 h-6 text-purple-600" />
                  </div>
                  <div>
                    <div class="font-semibold text-gray-900 group-hover/item:text-purple-900 transition-colors duration-300">Live Chat</div>
                    <div class="text-gray-600 group-hover/item:text-purple-600 transition-colors duration-300">Available 24/7</div>
                  </div>
                  <div class="ml-auto opacity-0 group-hover/item:opacity-100 transition-opacity duration-300">
                    <ArrowTopRightOnSquareIcon class="w-5 h-5 text-purple-600" />
                  </div>
                </div>
              </div>
            </div>
          </div>
          
          <!-- Office Locations Card -->
          <div class="group bg-white p-10 rounded-3xl border border-gray-200 shadow-lg hover:shadow-xl transition-all duration-500 relative overflow-hidden">
            <div class="absolute inset-0 bg-gradient-to-br from-purple-50 to-blue-50 opacity-0 group-hover:opacity-100 transition-opacity duration-500"></div>
            
            <div class="relative z-10">
              <div class="flex items-center space-x-4 mb-8">
                <div class="w-16 h-16 bg-gray-900 rounded-2xl flex items-center justify-center group-hover:scale-110 group-hover:bg-purple-900 transition-all duration-500">
                  <MapPinIcon class="w-8 h-8 text-white" />
                </div>
                <div>
                  <h3 class="text-2xl font-bold text-gray-900 group-hover:text-purple-900 transition-colors duration-300 font-heading">Our Offices</h3>
                  <p class="text-gray-600 group-hover:text-purple-600 transition-colors duration-300">Global presence, local expertise</p>
                </div>
              </div>
              
              <div class="space-y-6">
                <div class="office-item group/office p-6 border border-gray-200 rounded-2xl hover:border-blue-300 hover:bg-blue-50 transition-all duration-300">
                  <div class="flex items-start space-x-4">
                    <div class="w-10 h-10 bg-blue-100 rounded-xl flex items-center justify-center mt-1 group-hover/office:bg-blue-200 group-hover/office:scale-110 transition-all duration-300">
                      <span class="text-blue-600 font-bold text-sm">US</span>
                    </div>
                    <div class="flex-1">
                      <h4 class="font-bold text-gray-900 mb-2 group-hover/office:text-blue-900 transition-colors duration-300">United States</h4>
                      <p class="text-gray-600 text-sm leading-relaxed group-hover/office:text-blue-600 transition-colors duration-300">
                        8333 Bryan Dairy Rd,<br>
                        Seminole, FL 33777, US
                      </p>
                    </div>
                  </div>
                </div>
                
                <div class="office-item group/office p-6 border border-gray-200 rounded-2xl hover:border-green-300 hover:bg-green-50 transition-all duration-300">
                  <div class="flex items-start space-x-4">
                    <div class="w-10 h-10 bg-green-100 rounded-xl flex items-center justify-center mt-1 group-hover/office:bg-green-200 group-hover/office:scale-110 transition-all duration-300">
                      <span class="text-green-600 font-bold text-sm">LK</span>
                    </div>
                    <div class="flex-1">
                      <h4 class="font-bold text-gray-900 mb-2 group-hover/office:text-green-900 transition-colors duration-300">Sri Lanka</h4>
                      <p class="text-gray-600 text-sm leading-relaxed group-hover/office:text-green-600 transition-colors duration-300">
                        Level 12, One Galle Face Tower,<br>
                        Centre Road, Colombo 02, Sri Lanka
                      </p>
                    </div>
                  </div>
                </div>
              </div>
            </div>
          </div>

          <!-- Quick Response Card -->
          <div class="bg-gray-900 text-white p-10 rounded-3xl relative overflow-hidden">
            <div class="absolute inset-0 bg-gradient-to-r from-blue-600/20 to-purple-600/20"></div>
            
            <div class="relative z-10">
              <div class="flex items-center space-x-4 mb-6">
                <div class="w-12 h-12 bg-yellow-400 rounded-xl flex items-center justify-center">
                  <ClockIcon class="w-6 h-6 text-gray-900" />
                </div>
                <div>
                  <h4 class="text-xl font-bold">Quick Response</h4>
                  <p class="text-gray-300">We respond within 2 hours</p>
                </div>
              </div>
              
              <div class="grid grid-cols-2 gap-4 text-center">
                <div class="bg-white/10 p-4 rounded-2xl">
                  <div class="text-2xl font-bold text-yellow-400">< 2hrs</div>
                  <div class="text-sm text-gray-300">Response Time</div>
                </div>
                <div class="bg-white/10 p-4 rounded-2xl">
                  <div class="text-2xl font-bold text-green-400">24/7</div>
                  <div class="text-sm text-gray-300">Support</div>
                </div>
              </div>
            </div>
          </div>
        </div>
        
        <!-- Enhanced Contact Form -->
        <div class="contact-form">
          <div class="bg-white p-10 rounded-3xl border border-gray-200 shadow-lg relative overflow-hidden">
            <div class="absolute inset-0 bg-gradient-to-br from-gray-50 to-white opacity-50"></div>
            
            <div class="relative z-10">
              <div class="text-center mb-8">
                <h3 class="text-3xl font-bold text-gray-900 mb-4 font-heading">Start Your Project</h3>
                <p class="text-gray-600">Tell us about your vision and we'll make it reality</p>
              </div>
              
              <form @submit.prevent="submitForm" class="space-y-6">
                <div class="grid md:grid-cols-2 gap-6">
                  <div class="form-group">
                    <label for="name" class="block text-sm font-semibold text-gray-700 mb-3">Full Name *</label>
                    <div class="relative">
                      <input
                        type="text"
                        id="name"
                        v-model="form.name"
                        required
                        class="w-full px-5 py-4 bg-gray-50 border-2 border-gray-200 rounded-2xl text-gray-900 placeholder-gray-500 focus:outline-none focus:ring-2 focus:ring-blue-500 focus:border-blue-500 transition-all duration-300"
                        placeholder="John Doe"
                      >
                      <UserIcon class="absolute right-4 top-1/2 transform -translate-y-1/2 w-5 h-5 text-gray-400" />
                    </div>
                  </div>
                  
                  <div class="form-group">
                    <label for="email" class="block text-sm font-semibold text-gray-700 mb-3">Email Address *</label>
                    <div class="relative">
                      <input
                        type="email"
                        id="email"
                        v-model="form.email"
                        required
                        class="w-full px-5 py-4 bg-gray-50 border-2 border-gray-200 rounded-2xl text-gray-900 placeholder-gray-500 focus:outline-none focus:ring-2 focus:ring-blue-500 focus:border-blue-500 transition-all duration-300"
                        placeholder="john@company.com"
                      >
                      <EnvelopeIcon class="absolute right-4 top-1/2 transform -translate-y-1/2 w-5 h-5 text-gray-400" />
                    </div>
                  </div>
                </div>

                <div class="form-group">
                  <label for="company" class="block text-sm font-semibold text-gray-700 mb-3">Company</label>
                  <div class="relative">
                    <input
                      type="text"
                      id="company"
                      v-model="form.company"
                      class="w-full px-5 py-4 bg-gray-50 border-2 border-gray-200 rounded-2xl text-gray-900 placeholder-gray-500 focus:outline-none focus:ring-2 focus:ring-blue-500 focus:border-blue-500 transition-all duration-300"
                      placeholder="Your Company"
                    >
                    <BuildingOfficeIcon class="absolute right-4 top-1/2 transform -translate-y-1/2 w-5 h-5 text-gray-400" />
                  </div>
                </div>

                <div class="form-group">
                  <label for="budget" class="block text-sm font-semibold text-gray-700 mb-3">Project Budget</label>
                  <select
                    id="budget"
                    v-model="form.budget"
                    class="w-full px-5 py-4 bg-gray-50 border-2 border-gray-200 rounded-2xl text-gray-900 focus:outline-none focus:ring-2 focus:ring-blue-500 focus:border-blue-500 transition-all duration-300"
                  >
                    <option value="">Select budget range</option>
                    <option value="under-25k">Under $25,000</option>
                    <option value="25k-50k">$25,000 - $50,000</option>
                    <option value="50k-100k">$50,000 - $100,000</option>
                    <option value="100k-plus">$100,000+</option>
                  </select>
                </div>
                
                <div class="form-group">
                  <label for="message" class="block text-sm font-semibold text-gray-700 mb-3">Project Details *</label>
                  <textarea
                    id="message"
                    v-model="form.message"
                    required
                    rows="5"
                    class="w-full px-5 py-4 bg-gray-50 border-2 border-gray-200 rounded-2xl text-gray-900 placeholder-gray-500 focus:outline-none focus:ring-2 focus:ring-blue-500 focus:border-blue-500 transition-all duration-300 resize-none"
                    placeholder="Tell us about your project goals, timeline, and requirements..."
                  ></textarea>
                </div>
                
                <button 
                  type="submit" 
                  class="w-full bg-gray-900 text-white px-8 py-5 rounded-2xl font-semibold text-lg hover:bg-gray-800 transition-all duration-300 transform hover:scale-[1.02] flex items-center justify-center space-x-3 shadow-lg hover:shadow-xl"
                  :disabled="isSubmitting"
                >
                  <span>{{ isSubmitting ? 'Sending...' : 'Send Message' }}</span>
                  <PaperAirplaneIcon class="w-5 h-5" />
                </button>

                <div class="text-center pt-4">
                  <p class="text-sm text-gray-500">
                    By submitting this form, you agree to our 
                    <a href="#" class="text-blue-600 hover:text-blue-700 transition-colors duration-300">Privacy Policy</a>
                  </p>
                </div>
              </form>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
import { reactive, ref, onMounted } from 'vue'
import { gsap } from 'gsap'
import { ScrollTrigger } from 'gsap/ScrollTrigger'
import {
  EnvelopeIcon,
  PhoneIcon,
  MapPinIcon,
  UserIcon,
  BuildingOfficeIcon,
  ClockIcon,
  PaperAirplaneIcon,
  ChatBubbleLeftRightIcon,
  ArrowTopRightOnSquareIcon
} from '@heroicons/vue/24/outline'

const isSubmitting = ref(false)

const form = reactive({
  name: '',
  email: '',
  company: '',
  budget: '',
  message: ''
})

const submitForm = async () => {
  isSubmitting.value = true
  
  // Simulate form submission
  setTimeout(() => {
    console.log('Form submitted:', form)
    
    // Reset form
    Object.keys(form).forEach(key => {
      form[key] = ''
    })
    
    isSubmitting.value = false
    
    // Show success message (you can implement a toast notification here)
    alert('Thank you! We\'ll get back to you within 2 hours.')
  }, 2000)
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
    
    // Animate contact info
    gsap.fromTo('.contact-info > div',
      { opacity: 0, x: -50, scale: 0.9 },
      {
        opacity: 1,
        x: 0,
        scale: 1,
        duration: 0.8,
        stagger: 0.2,
        ease: 'back.out(1.7)',
        scrollTrigger: {
          trigger: '.contact-info',
          start: 'top 80%',
          toggleActions: 'play none none reverse'
        }
      }
    )
    
    // Animate contact form
    gsap.fromTo('.contact-form',
      { opacity: 0, x: 50, scale: 0.9 },
      {
        opacity: 1,
        x: 0,
        scale: 1,
        duration: 0.8,
        ease: 'back.out(1.7)',
        scrollTrigger: {
          trigger: '.contact-form',
          start: 'top 80%',
          toggleActions: 'play none none reverse'
        }
      }
    )

    // Animate form groups
    gsap.fromTo('.form-group',
      { opacity: 0, y: 20 },
      {
        opacity: 1,
        y: 0,
        duration: 0.5,
        stagger: 0.1,
        ease: 'power3.out',
        scrollTrigger: {
          trigger: '.form-group',
          start: 'top 85%',
          toggleActions: 'play none none reverse'
        }
      }
    )

    // Animate floating elements
    gsap.to('.contact-float-1', { y: -20, duration: 3, yoyo: true, repeat: -1, ease: 'sine.inOut' })
    gsap.to('.contact-float-2', { y: -30, duration: 4, yoyo: true, repeat: -1, ease: 'sine.inOut', delay: 1 })
    gsap.to('.contact-float-3', { y: -25, duration: 3.5, yoyo: true, repeat: -1, ease: 'sine.inOut', delay: 2 })
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

.contact-float {
  position: absolute;
  width: 12px;
  height: 12px;
  background: linear-gradient(45deg, #3b82f6, #10b981);
  border-radius: 50%;
  opacity: 0.6;
}

.contact-float-1 { top: 15%; left: 5%; }
.contact-float-2 { top: 60%; right: 10%; }
.contact-float-3 { bottom: 25%; left: 15%; }
</style>