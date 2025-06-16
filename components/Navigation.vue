<template>
  <nav class="fixed top-0 left-0 right-0 z-50 bg-gray-900/95 backdrop-blur-sm border-b border-gray-800 transition-all duration-300">
    <div class="container-custom relative">
      <div class="flex items-center justify-between h-16 md:h-20">
        <!-- Logo -->
        <div class="flex items-center space-x-3">
          <div class="w-10 h-10 bg-lime-400 rounded-lg flex items-center justify-center">
            <span class="text-gray-900 font-bold text-xl">MB</span>
          </div>
          <span class="text-xl md:text-2xl font-bold text-white font-heading">Tech Now</span>
        </div>
        
        <!-- Desktop Menu -->
        <div class="hidden lg:flex items-center space-x-8">
          <!-- Services Dropdown -->
          <div class="relative group">
            <button 
              @click="toggleDropdown('services')"
              @mouseenter="showDropdown('services')"
              @mouseleave="hideDropdown('services')"
              class="flex items-center text-gray-300 hover:text-white transition-colors duration-300 font-medium"
            >
              Services
              <svg class="w-4 h-4 ml-1 transition-transform duration-300" 
                   :class="{ 'rotate-180': activeDropdown === 'services' }"
                   fill="none" stroke="currentColor" viewBox="0 0 24 24">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 9l-7 7-7-7"></path>
              </svg>
            </button>
            
            <!-- Services Dropdown Menu -->
            <div 
              v-show="activeDropdown === 'services'"
              @mouseenter="showDropdown('services')"
              @mouseleave="hideDropdown('services')"
              class="absolute top-full left-0 mt-2 w-80 bg-gray-800/95 backdrop-blur-sm border border-gray-700 rounded-xl shadow-2xl overflow-hidden"
            >
              <div class="p-6">
                <div class="grid grid-cols-1 gap-4">
                  <div v-for="service in servicesDropdown" :key="service.name" 
                       class="group/item p-3 rounded-lg hover:bg-gray-700/50 transition-all duration-300 cursor-pointer">
                    <div class="flex items-start space-x-3">
                      <div class="w-10 h-10 bg-lime-400/10 rounded-lg flex items-center justify-center group-hover/item:bg-lime-400/20 transition-colors duration-300">
                        <div v-html="service.icon" class="w-5 h-5 text-lime-400"></div>
                      </div>
                      <div class="flex-1">
                        <h4 class="text-white font-semibold group-hover/item:text-lime-400 transition-colors duration-300">{{ service.name }}</h4>
                        <p class="text-gray-400 text-sm mt-1">{{ service.description }}</p>
                      </div>
                    </div>
                  </div>
                </div>
                <div class="mt-4 pt-4 border-t border-gray-700">
                  <a href="#services" class="inline-flex items-center text-lime-400 hover:text-lime-300 transition-colors duration-300 font-medium">
                    View all services
                    <svg class="w-4 h-4 ml-1" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                      <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M17 8l4 4m0 0l-4 4m4-4H3"></path>
                    </svg>
                  </a>
                </div>
              </div>
            </div>
          </div>

          <!-- Solutions Dropdown -->
          <div class="relative group">
            <button 
              @click="toggleDropdown('solutions')"
              @mouseenter="showDropdown('solutions')"
              @mouseleave="hideDropdown('solutions')"
              class="flex items-center text-gray-300 hover:text-white transition-colors duration-300 font-medium"
            >
              Solutions
              <svg class="w-4 h-4 ml-1 transition-transform duration-300" 
                   :class="{ 'rotate-180': activeDropdown === 'solutions' }"
                   fill="none" stroke="currentColor" viewBox="0 0 24 24">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 9l-7 7-7-7"></path>
              </svg>
            </button>
            
            <!-- Solutions Dropdown Menu -->
            <div 
              v-show="activeDropdown === 'solutions'"
              @mouseenter="showDropdown('solutions')"
              @mouseleave="hideDropdown('solutions')"
              class="absolute top-full left-0 mt-2 w-96 bg-gray-800/95 backdrop-blur-sm border border-gray-700 rounded-xl shadow-2xl overflow-hidden"
            >
              <div class="p-6">
                <div class="grid grid-cols-2 gap-4">
                  <div v-for="solution in solutionsDropdown" :key="solution.name" 
                       class="group/item p-3 rounded-lg hover:bg-gray-700/50 transition-all duration-300 cursor-pointer">
                    <div class="text-center">
                      <div class="w-12 h-12 bg-lime-400/10 rounded-lg flex items-center justify-center mx-auto mb-3 group-hover/item:bg-lime-400/20 transition-colors duration-300">
                        <div v-html="solution.icon" class="w-6 h-6 text-lime-400"></div>
                      </div>
                      <h4 class="text-white font-semibold text-sm group-hover/item:text-lime-400 transition-colors duration-300">{{ solution.name }}</h4>
                      <p class="text-gray-400 text-xs mt-1">{{ solution.description }}</p>
                    </div>
                  </div>
                </div>
                <div class="mt-4 pt-4 border-t border-gray-700">
                  <a href="#portfolio" class="inline-flex items-center text-lime-400 hover:text-lime-300 transition-colors duration-300 font-medium">
                    View all solutions
                    <svg class="w-4 h-4 ml-1" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                      <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M17 8l4 4m0 0l-4 4m4-4H3"></path>
                    </svg>
                  </a>
                </div>
              </div>
            </div>
          </div>

          <!-- Regular Menu Items -->
          <a v-for="item in regularMenuItems" :key="item.name" :href="item.href" 
             class="text-gray-300 hover:text-white transition-colors duration-300 font-medium">
            {{ item.name }}
          </a>

          <button class="inline-flex items-center bg-lime-400 text-gray-900 px-6 py-3 rounded-full font-semibold hover:bg-lime-300 transition-all duration-300 transform hover:scale-105">
            <span>Contact us</span>
            <div class="ml-2 w-6 h-6 bg-gray-900 rounded-full flex items-center justify-center">
              <svg class="w-3 h-3 text-lime-400" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M7 17L17 7M17 7H7M17 7V17"></path>
              </svg>
            </div>
          </button>
        </div>
        
        <!-- Mobile Menu Button -->
        <button @click="mobileMenuOpen = !mobileMenuOpen" class="lg:hidden text-white">
          <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24">
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" 
                  :d="mobileMenuOpen ? 'M6 18L18 6M6 6l12 12' : 'M4 6h16M4 12h16M4 18h16'"></path>
          </svg>
        </button>
      </div>
      
      <!-- Mobile Menu -->
      <div v-show="mobileMenuOpen" class="lg:hidden bg-gray-800 border-t border-gray-700 rounded-b-lg shadow-lg mt-1 p-4">
        <div class="flex flex-col space-y-4">
          <!-- Mobile Services -->
          <div class="border-b border-gray-700 pb-4">
            <button @click="mobileServicesOpen = !mobileServicesOpen" 
                    class="flex items-center justify-between w-full text-gray-300 hover:text-white transition-colors duration-300 font-medium">
              Services
              <svg class="w-4 h-4 transition-transform duration-300" 
                   :class="{ 'rotate-180': mobileServicesOpen }"
                   fill="none" stroke="currentColor" viewBox="0 0 24 24">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 9l-7 7-7-7"></path>
              </svg>
            </button>
            <div v-show="mobileServicesOpen" class="mt-3 pl-4 space-y-2">
              <a v-for="service in servicesDropdown" :key="service.name" 
                 href="#" class="block text-sm text-gray-400 hover:text-white transition-colors duration-300">
                {{ service.name }}
              </a>
            </div>
          </div>

          <!-- Mobile Solutions -->
          <div class="border-b border-gray-700 pb-4">
            <button @click="mobileSolutionsOpen = !mobileSolutionsOpen" 
                    class="flex items-center justify-between w-full text-gray-300 hover:text-white transition-colors duration-300 font-medium">
              Solutions
              <svg class="w-4 h-4 transition-transform duration-300" 
                   :class="{ 'rotate-180': mobileSolutionsOpen }"
                   fill="none" stroke="currentColor" viewBox="0 0 24 24">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 9l-7 7-7-7"></path>
              </svg>
            </button>
            <div v-show="mobileSolutionsOpen" class="mt-3 pl-4 space-y-2">
              <a v-for="solution in solutionsDropdown" :key="solution.name" 
                 href="#" class="block text-sm text-gray-400 hover:text-white transition-colors duration-300">
                {{ solution.name }}
              </a>
            </div>
          </div>

          <!-- Regular Mobile Items -->
          <a v-for="item in regularMenuItems" :key="item.name" :href="item.href" 
             class="text-gray-300 hover:text-white transition-colors duration-300 font-medium">
            {{ item.name }}
          </a>

          <button class="inline-flex items-center justify-center bg-lime-400 text-gray-900 px-6 py-3 rounded-full font-semibold hover:bg-lime-300 transition-all duration-300 w-full">
            <span>Contact us</span>
            <div class="ml-2 w-6 h-6 bg-gray-900 rounded-full flex items-center justify-center">
              <svg class="w-3 h-3 text-lime-400" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M7 17L17 7M17 7H7M17 7V17"></path>
              </svg>
            </div>
          </button>
        </div>
      </div>

      <!-- Dropdown Backdrop -->
      <div v-show="activeDropdown" 
           @click="activeDropdown = null"
           class="fixed inset-0 bg-black/20 backdrop-blur-sm -z-10"></div>
    </div>
  </nav>
</template>

<script setup>
import { ref, onMounted, onUnmounted } from 'vue'

const mobileMenuOpen = ref(false)
const mobileServicesOpen = ref(false)
const mobileSolutionsOpen = ref(false)
const activeDropdown = ref(null)
let hideTimeout = null

const regularMenuItems = [
  { name: 'About Us', href: '#about' },
  { name: 'Careers', href: '#careers' },
  { name: 'Contact', href: '#contact' }
]

const servicesDropdown = [
  {
    name: 'Digital Transformation',
    description: 'Modernize your business processes and technology stack',
    icon: '<svg fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M13 10V3L4 14h7v7l9-11h-7z"></path></svg>'
  },
  {
    name: 'Cloud Solutions',
    description: 'Scalable cloud infrastructure and migration services',
    icon: '<svg fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M7 16a4 4 0 01-.88-7.903A5 5 0 1115.9 6L16 6a5 5 0 011 9.9M9 19l3 3m0 0l3-3m-3 3V10"></path></svg>'
  },
  {
    name: 'AI & Machine Learning',
    description: 'Intelligent automation and predictive analytics',
    icon: '<svg fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9.663 17h4.673M12 3v1m6.364 1.636l-.707.707M21 12h-1M4 12H3m3.343-5.657l-.707-.707m2.828 9.9a5 5 0 117.072 0l-.548.547A3.374 3.374 0 0014 18.469V19a2 2 0 11-4 0v-.531c0-.895-.356-1.754-.988-2.386l-.548-.547z"></path></svg>'
  },
  {
    name: 'Cybersecurity',
    description: 'Comprehensive security solutions and compliance',
    icon: '<svg fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 12l2 2 4-4m5.618-4.016A11.955 11.955 0 0112 2.944a11.955 11.955 0 01-8.618 3.04A12.02 12.02 0 003 9c0 5.591 3.824 10.29 9 11.622 5.176-1.332 9-6.03 9-11.622 0-1.042-.133-2.052-.382-3.016z"></path></svg>'
  }
]

const solutionsDropdown = [
  {
    name: 'Manufacturing',
    description: 'Industry 4.0 solutions',
    icon: '<svg fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19.428 15.428a2 2 0 00-1.022-.547l-2.387-.477a6 6 0 00-3.86.517l-.318.158a6 6 0 01-3.86.517L6.05 15.21a2 2 0 00-1.806.547M8 4h8l-1 1v5.172a2 2 0 00.586 1.414l5 5c1.26 1.26.367 3.414-1.415 3.414H4.828c-1.782 0-2.674-2.154-1.414-3.414l5-5A2 2 0 009 10.172V5L8 4z"></path></svg>'
  },
  {
    name: 'Healthcare',
    description: 'HIPAA compliant systems',
    icon: '<svg fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4.318 6.318a4.5 4.5 0 000 6.364L12 20.364l7.682-7.682a4.5 4.5 0 00-6.364-6.364L12 7.636l-1.318-1.318a4.5 4.5 0 00-6.364 0z"></path></svg>'
  },
  {
    name: 'Financial Services',
    description: 'Secure fintech solutions',
    icon: '<svg fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 8c-1.657 0-3 .895-3 2s1.343 2 3 2 3 .895 3 2-1.343 2-3 2m0-8c1.11 0 2.08.402 2.599 1M12 8V7m0 1v8m0 0v1m0-1c-1.11 0-2.08-.402-2.599-1M21 12a9 9 0 11-18 0 9 9 0 0118 0z"></path></svg>'
  },
  {
    name: 'E-commerce',
    description: 'Scalable retail platforms',
    icon: '<svg fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M16 11V7a4 4 0 00-8 0v4M5 9h14l1 12H4L5 9z"></path></svg>'
  }
]

const showDropdown = (dropdown) => {
  if (hideTimeout) {
    clearTimeout(hideTimeout)
    hideTimeout = null
  }
  activeDropdown.value = dropdown
}

const hideDropdown = (dropdown) => {
  hideTimeout = setTimeout(() => {
    if (activeDropdown.value === dropdown) {
      activeDropdown.value = null
    }
  }, 150)
}

const toggleDropdown = (dropdown) => {
  activeDropdown.value = activeDropdown.value === dropdown ? null : dropdown
}

const handleClickOutside = (event) => {
  const nav = event.target.closest('nav')
  if (!nav) {
    activeDropdown.value = null
    mobileMenuOpen.value = false
  }
}

onMounted(() => {
  document.addEventListener('click', handleClickOutside)
})

onUnmounted(() => {
  document.removeEventListener('click', handleClickOutside)
  if (hideTimeout) {
    clearTimeout(hideTimeout)
  }
})
</script>