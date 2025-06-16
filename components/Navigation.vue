<template>
  <nav class="fixed top-0 left-0 right-0 z-50 bg-gray-900/95 backdrop-blur-sm border-b border-gray-800 transition-all duration-300">
    <div class="container-custom">
      <div class="flex items-center justify-between h-16 md:h-20">
        <!-- Logo -->
        <div class="flex items-center space-x-3">
          <span class="text-xl md:text-2xl font-bold text-white font-heading">MB Tech Now</span>
        </div>
        
        <!-- Desktop Menu -->
        <div class="hidden lg:flex items-center space-x-8">
          <a v-for="item in menuItems" :key="item.name" :href="item.href" 
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
          <a v-for="item in menuItems" :key="item.name" :href="item.href" 
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
    </div>
  </nav>
</template>

<script setup>
import { ref } from 'vue'

const mobileMenuOpen = ref(false)

const menuItems = [
  { name: 'Services', href: '#services' },
  { name: 'Portfolio', href: '#portfolio' },
  { name: 'About Us', href: '#about' },
  { name: 'Careers', href: '#careers' },
  { name: 'Contact', href: '#contact' },
  { name: 'FAQs', href: '#faqs' }
]
</script>