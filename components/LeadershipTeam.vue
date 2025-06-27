<template>
  <section class="section-padding bg-gradient-to-br from-gray-50 via-white to-gray-50 relative overflow-hidden">
    <!-- Background Pattern -->
    <div class="absolute inset-0 opacity-5">
      <div class="absolute inset-0" style="background-image: radial-gradient(circle at 25% 75%, rgba(59, 130, 246, 0.1) 0%, transparent 50%), radial-gradient(circle at 75% 25%, rgba(147, 51, 234, 0.1) 0%, transparent 50%);"></div>
    </div>

    <div class="container-custom relative z-10">
      <!-- Header -->
      <div class="max-w-4xl mx-auto text-center mb-20">
        <div class="inline-flex items-center bg-blue-100 text-blue-800 px-6 py-3 rounded-full text-sm font-semibold mb-8">
          <span class="w-2 h-2 bg-blue-500 rounded-full mr-3"></span>
          LEADERSHIP TEAM
        </div>
        
        <h2 class="text-5xl md:text-6xl lg:text-7xl font-bold mb-8 text-gray-900 font-heading leading-tight">
          Meet The
          <span class="block gradient-text animate-gradient">Visionaries</span>
          <span class="block text-4xl md:text-5xl lg:text-6xl text-gray-700">Behind Our Success</span>
        </h2>
        
        <p class="text-xl text-gray-600 leading-relaxed">
          Our leadership team combines decades of experience with a passion for innovation, 
          driving our mission to transform enterprises through cutting-edge technology.
        </p>
      </div>

      <!-- Leadership Grid -->
      <div class="grid md:grid-cols-2 lg:grid-cols-3 gap-12 mb-20">
        <div v-for="(leader, index) in leaders" :key="leader.name"
             class="leader-card group relative bg-white p-8 rounded-3xl border border-gray-200 hover:border-blue-300 transition-all duration-500 cursor-pointer overflow-hidden"
             @mouseenter="handleLeaderHover(index, true)"
             @mouseleave="handleLeaderHover(index, false)">
          
          <!-- Card Background Animation -->
          <div class="absolute inset-0 bg-gradient-to-br from-blue-50 to-purple-50 opacity-0 group-hover:opacity-100 transition-opacity duration-500"></div>
          
          <div class="relative z-10 text-center">
            <!-- Avatar -->
            <div class="relative mb-6">
              <div :class="leader.avatarClass" class="w-24 h-24 rounded-2xl flex items-center justify-center mx-auto mb-4 group-hover:scale-110 transition-transform duration-500 shadow-lg">
                <span class="text-2xl font-bold text-white">{{ leader.initials }}</span>
              </div>
              <!-- Status Badge -->
              <div class="absolute -bottom-2 left-1/2 transform -translate-x-1/2 bg-green-500 text-white text-xs px-3 py-1 rounded-full opacity-0 group-hover:opacity-100 transition-opacity duration-500">
                {{ leader.status }}
              </div>
            </div>
            
            <!-- Name & Title -->
            <h3 class="text-2xl font-bold mb-2 text-gray-900 group-hover:text-blue-900 transition-colors duration-300 font-heading">
              {{ leader.name }}
            </h3>
            <div class="text-blue-600 font-semibold mb-4">{{ leader.position }}</div>
            
            <!-- Bio -->
            <p class="text-gray-600 leading-relaxed mb-6 group-hover:text-gray-700 transition-colors duration-300">
              {{ leader.bio }}
            </p>
            
            <!-- Expertise -->
            <div class="mb-6">
              <div class="text-sm font-semibold text-gray-700 mb-3">Expertise</div>
              <div class="flex flex-wrap gap-2 justify-center">
                <span v-for="skill in leader.expertise" :key="skill"
                      class="px-3 py-1 bg-gray-100 text-gray-700 text-xs rounded-full group-hover:bg-blue-100 group-hover:text-blue-700 transition-colors duration-300">
                  {{ skill }}
                </span>
              </div>
            </div>
            
            <!-- Achievement -->
            <div class="bg-gray-50 p-4 rounded-2xl group-hover:bg-white transition-colors duration-300">
              <div class="text-2xl font-bold text-blue-600 mb-1">{{ leader.achievement.value }}</div>
              <div class="text-xs text-gray-500">{{ leader.achievement.label }}</div>
            </div>
            
            <!-- Social Links -->
            <div class="flex justify-center space-x-4 mt-6 opacity-0 group-hover:opacity-100 transition-opacity duration-500">
              <button class="w-8 h-8 bg-blue-100 rounded-full flex items-center justify-center hover:bg-blue-200 transition-colors duration-300">
                <svg class="w-4 h-4 text-blue-600" fill="currentColor" viewBox="0 0 24 24">
                  <path d="M20.447 20.452h-3.554v-5.569c0-1.328-.027-3.037-1.852-3.037-1.853 0-2.136 1.445-2.136 2.939v5.667H9.351V9h3.414v1.561h.046c.477-.9 1.637-1.85 3.37-1.85 3.601 0 4.267 2.37 4.267 5.455v6.286zM5.337 7.433c-1.144 0-2.063-.926-2.063-2.065 0-1.138.92-2.063 2.063-2.063 1.14 0 2.064.925 2.064 2.063 0 1.139-.925 2.065-2.064 2.065zm1.782 13.019H3.555V9h3.564v11.452zM22.225 0H1.771C.792 0 0 .774 0 1.729v20.542C0 23.227.792 24 1.771 24h20.451C23.2 24 24 23.227 24 22.271V1.729C24 .774 23.2 0 22.222 0h.003z"/>
                </svg>
              </button>
              <button class="w-8 h-8 bg-gray-100 rounded-full flex items-center justify-center hover:bg-gray-200 transition-colors duration-300">
                <svg class="w-4 h-4 text-gray-600" fill="currentColor" viewBox="0 0 24 24">
                  <path d="M23.953 4.57a10 10 0 01-2.825.775 4.958 4.958 0 002.163-2.723c-.951.555-2.005.959-3.127 1.184a4.92 4.92 0 00-8.384 4.482C7.69 8.095 4.067 6.13 1.64 3.162a4.822 4.822 0 00-.666 2.475c0 1.71.87 3.213 2.188 4.096a4.904 4.904 0 01-2.228-.616v.06a4.923 4.923 0 003.946 4.827 4.996 4.996 0 01-2.212.085 4.936 4.936 0 004.604 3.417 9.867 9.867 0 01-6.102 2.105c-.39 0-.779-.023-1.17-.067a13.995 13.995 0 007.557 2.209c9.053 0 13.998-7.496 13.998-13.985 0-.21 0-.42-.015-.63A9.935 9.935 0 0024 4.59z"/>
                </svg>
              </button>
            </div>
          </div>
        </div>
      </div>

      <!-- Board & Advisors -->
      <div class="max-w-5xl mx-auto">
        <div class="bg-white p-12 rounded-3xl border border-gray-200 relative overflow-hidden">
          <div class="text-center mb-12">
            <h3 class="text-3xl md:text-4xl font-bold mb-4 text-gray-900 font-heading">
              Board of Directors & Advisors
            </h3>
            <p class="text-lg text-gray-600">
              Strategic guidance from industry veterans and technology pioneers
            </p>
          </div>
          
          <div class="grid md:grid-cols-2 lg:grid-cols-4 gap-8">
            <div v-for="advisor in advisors" :key="advisor.name" class="advisor-card text-center group cursor-pointer">
              <div :class="advisor.avatarClass" class="w-16 h-16 rounded-xl flex items-center justify-center mx-auto mb-4 group-hover:scale-110 transition-transform duration-300">
                <span class="text-lg font-bold text-white">{{ advisor.initials }}</span>
              </div>
              <h4 class="font-bold text-gray-900 mb-1 group-hover:text-blue-900 transition-colors duration-300">{{ advisor.name }}</h4>
              <div class="text-sm text-blue-600 mb-2">{{ advisor.role }}</div>
              <div class="text-xs text-gray-500">{{ advisor.company }}</div>
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

const leaders = [
  {
    name: 'Michael Brown',
    position: 'CEO & Founder',
    initials: 'MB',
    avatarClass: 'bg-gradient-to-r from-blue-600 to-purple-600',
    bio: 'Visionary leader with 20+ years in enterprise technology. Founded MB Tech Now with the mission to revolutionize digital transformation.',
    expertise: ['Digital Strategy', 'Enterprise Architecture', 'AI Innovation'],
    achievement: { value: '15+', label: 'Years Leadership' },
    status: 'Available'
  },
  {
    name: 'Sarah Chen',
    position: 'CTO & Co-Founder',
    initials: 'SC',
    avatarClass: 'bg-gradient-to-r from-green-600 to-blue-600',
    bio: 'Technology architect and innovation driver. Leads our technical vision and oversees all engineering initiatives.',
    expertise: ['Cloud Architecture', 'System Design', 'Tech Innovation'],
    achievement: { value: '500+', label: 'Projects Delivered' },
    status: 'Available'
  },
  {
    name: 'David Rodriguez',
    position: 'VP of Engineering',
    initials: 'DR',
    avatarClass: 'bg-gradient-to-r from-purple-600 to-pink-600',
    bio: 'Engineering excellence advocate with expertise in scalable systems and team leadership across global development teams.',
    expertise: ['Team Leadership', 'Scalable Systems', 'DevOps'],
    achievement: { value: '200+', label: 'Engineers Led' },
    status: 'Available'
  },
  {
    name: 'Emily Johnson',
    position: 'Chief Strategy Officer',
    initials: 'EJ',
    avatarClass: 'bg-gradient-to-r from-orange-600 to-red-600',
    bio: 'Strategic business leader focused on market expansion and client success. Drives our growth initiatives and partnerships.',
    expertise: ['Business Strategy', 'Market Analysis', 'Client Success'],
    achievement: { value: '$2.3B+', label: 'Client Value Generated' },
    status: 'Available'
  },
  {
    name: 'James Wilson',
    position: 'VP of Security',
    initials: 'JW',
    avatarClass: 'bg-gradient-to-r from-gray-700 to-gray-900',
    bio: 'Cybersecurity expert ensuring enterprise-grade security across all our solutions and client implementations.',
    expertise: ['Cybersecurity', 'Compliance', 'Risk Management'],
    achievement: { value: '0', label: 'Security Breaches' },
    status: 'Available'
  },
  {
    name: 'Lisa Park',
    position: 'Chief People Officer',
    initials: 'LP',
    avatarClass: 'bg-gradient-to-r from-teal-600 to-green-600',
    bio: 'Human resources leader building world-class teams and fostering a culture of innovation and excellence.',
    expertise: ['Team Building', 'Culture Development', 'Talent Acquisition'],
    achievement: { value: '95%', label: 'Employee Satisfaction' },
    status: 'Available'
  }
]

const advisors = [
  {
    name: 'Robert Kim',
    role: 'Board Chairman',
    company: 'Former IBM Executive',
    initials: 'RK',
    avatarClass: 'bg-gradient-to-r from-blue-700 to-indigo-700'
  },
  {
    name: 'Maria Garcia',
    role: 'Strategic Advisor',
    company: 'Ex-Microsoft VP',
    initials: 'MG',
    avatarClass: 'bg-gradient-to-r from-green-700 to-emerald-700'
  },
  {
    name: 'John Smith',
    role: 'Technology Advisor',
    company: 'Former Google CTO',
    initials: 'JS',
    avatarClass: 'bg-gradient-to-r from-purple-700 to-violet-700'
  },
  {
    name: 'Anna Lee',
    role: 'Investment Advisor',
    company: 'Venture Partner',
    initials: 'AL',
    avatarClass: 'bg-gradient-to-r from-pink-700 to-rose-700'
  }
]

const handleLeaderHover = (index, isHover) => {
  if (process.client) {
    const card = document.querySelectorAll('.leader-card')[index]
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
        duration: 3,
        ease: 'none',
        repeat: -1
      }
    )
    
    // Animate leader cards
    gsap.fromTo('.leader-card',
      { opacity: 0, y: 50, scale: 0.9 },
      {
        opacity: 1,
        y: 0,
        scale: 1,
        duration: 0.8,
        stagger: 0.15,
        ease: 'back.out(1.7)',
        scrollTrigger: {
          trigger: '.leader-card',
          start: 'top 85%',
          toggleActions: 'play none none reverse'
        }
      }
    )
    
    // Animate advisor cards
    gsap.fromTo('.advisor-card',
      { opacity: 0, y: 30 },
      {
        opacity: 1,
        y: 0,
        duration: 0.6,
        stagger: 0.1,
        ease: 'back.out(1.7)',
        scrollTrigger: {
          trigger: '.advisor-card',
          start: 'top 85%',
          toggleActions: 'play none none reverse'
        }
      }
    )
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
</style>