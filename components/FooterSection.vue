<template>
  <footer class="bg-gray-900 text-white">
    <div class="container-custom py-16">
      <div class="grid lg:grid-cols-4 gap-8">
        <!-- Company Info -->
        <div class="lg:col-span-1">
          <div class="flex items-center space-x-3 mb-6">
            <div class="w-10 h-10 bg-white rounded-lg flex items-center justify-center">
              <span class="text-gray-900 font-bold text-xl">MB</span>
            </div>
            <span class="text-xl font-bold">Tech Now</span>
          </div>
          <p class="text-gray-400 mb-6">
            Your Unified Platform for Digital Transformation. We are the catalyst for your enterprise's digital evolution.
          </p>
          <div class="flex space-x-4">
            <a href="#" class="w-10 h-10 bg-gray-800 rounded-full flex items-center justify-center hover:bg-gray-700 transition-colors">
              <span class="text-white">📧</span>
            </a>
            <a href="#" class="w-10 h-10 bg-gray-800 rounded-full flex items-center justify-center hover:bg-gray-700 transition-colors">
              <span class="text-white">💼</span>
            </a>
            <a href="#" class="w-10 h-10 bg-gray-800 rounded-full flex items-center justify-center hover:bg-gray-700 transition-colors">
              <span class="text-white">🐦</span>
            </a>
          </div>
        </div>
        
        <!-- Quick Links -->
        <div>
          <h3 class="text-white font-semibold mb-4">Quick Links</h3>
          <ul class="space-y-2">
            <li v-for="link in quickLinks" :key="link.name">
              <a :href="link.href" class="text-gray-400 hover:text-white transition-colors">
                {{ link.name }}
              </a>
            </li>
          </ul>
        </div>
        
        <!-- Resources -->
        <div>
          <h3 class="text-white font-semibold mb-4">Resources</h3>
          <ul class="space-y-2">
            <li v-for="resource in resources" :key="resource.name">
              <a :href="resource.href" class="text-gray-400 hover:text-white transition-colors">
                {{ resource.name }}
              </a>
            </li>
          </ul>
        </div>
        
        <!-- Newsletter -->
        <div>
          <h3 class="text-white font-semibold mb-4">Subscribe Today</h3>
          <p class="text-gray-400 mb-4">See What's New Now</p>
          <div class="flex">
            <input
              type="email"
              placeholder="Enter your email"
              class="flex-1 px-4 py-2 bg-gray-800 border border-gray-700 rounded-l-lg text-white placeholder-gray-400 focus:outline-none focus:ring-2 focus:ring-white"
            >
            <button class="px-4 py-2 bg-white text-gray-900 rounded-r-lg hover:bg-gray-100 transition-colors font-semibold">
              →
            </button>
          </div>
        </div>
      </div>
      
      <div class="border-t border-gray-800 mt-12 pt-8 text-center">
        <p class="text-gray-400">
          © 2025 MB Tech Now - All Rights Reserved.
        </p>
      </div>
    </div>
  </footer>
</template>

<script setup>
const quickLinks = [
  { name: 'Home', href: '#' },
  { name: 'About Us', href: '#about' },
  { name: 'Services', href: '#services' },
  { name: 'Team', href: '#team' },
  { name: 'Portfolio', href: '#portfolio' },
  { name: 'Blog', href: '#blog' },
  { name: 'Contact Us', href: '#contact' },
  { name: 'Support', href: '#support' }
]

const resources = [
  { name: 'Get Immediate Consulting', href: '#consulting' },
  { name: 'See Success Stories', href: '#stories' },
  { name: 'Read the Docs', href: '#docs' },
  { name: 'Join Events', href: '#events' },
  { name: 'Explore the Library', href: '#library' },
  { name: 'Contribute to Open Source', href: '#opensource' },
  { name: 'Learn About Ethical Practices', href: '#ethics' },
  { name: 'Contact Us About Site Problems', href: '#problems' }
]
</script>