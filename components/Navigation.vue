<template>
  <nav class="fixed top-0 left-0 right-0 z-50 bg-white/95 backdrop-blur-sm border-b border-gray-100 transition-all duration-300">
    <div class="container-custom">
      <div class="flex items-center justify-between h-16 md:h-20">
        <!-- Logo -->
        <div class="flex items-center space-x-3">
          <div class="w-10 h-10 bg-gray-900 rounded-lg flex items-center justify-center">
            <span class="text-white font-bold text-xl">MB</span>
          </div>
          <span class="text-xl md:text-2xl font-bold text-gray-900">Tech Now</span>
        </div>
        
        <!-- Desktop Menu -->
        <div class="hidden lg:flex items-center space-x-8">
          <a v-for="item in menuItems" :key="item.name" :href="item.href" 
             class="text-gray-600 hover:text-gray-900 transition-colors duration-300 font-medium">
            {{ item.name }}
          </a>
          <button class="btn-primary">
            Contact us →
          </button>
        </div>
        
        <!-- Mobile Menu Button -->
        <button @click="mobileMenuOpen = !mobileMenuOpen" class="lg:hidden text-gray-900">
          <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24">
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" 
                  :d="mobileMenuOpen ? 'M6 18L18 6M6 6l12 12' : 'M4 6h16M4 12h16M4 18h16'"></path>
          </svg>
        </button>
      </div>
      
      <!-- Mobile Menu -->
      <div v-show="mobileMenuOpen" class="lg:hidden bg-white border-t border-gray-100 rounded-b-lg shadow-lg mt-1 p-4">
        <div class="flex flex-col space-y-4">
          <a v-for="item in menuItems" :key="item.name" :href="item.href" 
             class="text-gray-600 hover:text-gray-900 transition-colors duration-300 font-medium">
            {{ item.name }}
          </a>
          <button class="btn-primary w-full">
            Contact us →
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