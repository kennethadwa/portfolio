<script setup>
import { ref } from 'vue'

const isMobileMenuOpen = ref(false)

const navLinks = [
  { name: 'Home', href: '#home' },
  { name: 'About', href: '#about' },
  { name: 'Skills', href: '#skills' },
  { name: 'Projects', href: '#projects' },
  { name: 'Experience', href: '#experience' },
  { name: 'Contact', href: '#contact' },
]

// Smooth scroll handler na may offset para sa floating navbar
const scrollToSection = (e, href) => {
  e.preventDefault()
  const target = document.querySelector(href)
  if (target) {
    const navOffset = 90
    const targetPosition = target.getBoundingClientRect().top + window.pageYOffset - navOffset
    
    window.scrollTo({
      top: targetPosition,
      behavior: 'smooth'
    })
    
    isMobileMenuOpen.value = false
  }
}
</script>

<template>
  <header class="fixed top-4 inset-x-0 z-50 max-w-5xl mx-auto px-4 pointer-events-none">
    <!-- Floating Dark Glassmorphic Pill -->
    <nav class="pointer-events-auto bg-slate-900/80 backdrop-blur-xl border border-slate-800/90 shadow-2xl shadow-black/50 rounded-2xl px-5 h-14 flex items-center justify-between transition-all">
      
      <!-- Logo / Brand -->
      <a 
        href="#home" 
        @click="scrollToSection($event, '#home')"
        class="text-sm sm:text-base font-bold tracking-tight text-white flex items-center gap-2 group cursor-pointer"
      >
        <span class="w-7 h-7 rounded-lg bg-teal-400 flex items-center justify-center text-slate-950 font-mono font-black text-xs shadow-md shadow-teal-500/20 group-hover:scale-105 transition-transform">
          JK
        </span>
        <span class="group-hover:text-teal-300 transition-colors">Ortigueras</span>
      </a>

      <!-- Desktop Navlinks with Aurora Accents -->
      <ul class="hidden md:flex items-center gap-1">
        <li v-for="link in navLinks" :key="link.name">
          <a 
            :href="link.href" 
            @click="scrollToSection($event, link.href)"
            class="px-3 py-1.5 rounded-lg text-xs font-mono tracking-wider uppercase text-slate-300 hover:text-teal-300 hover:bg-slate-800/70 transition-all cursor-pointer"
          >
            {{ link.name }}
          </a>
        </li>
      </ul>

      <!-- High-Contrast Action Button -->
      <div class="hidden md:flex items-center">
        <a 
          href="#contact" 
          @click="scrollToSection($event, '#contact')"
          class="text-xs font-mono font-bold uppercase tracking-wider px-4 py-1.5 rounded-xl bg-teal-400 hover:bg-teal-300 text-slate-950 transition-all shadow-md shadow-teal-500/20 hover:shadow-teal-400/30 hover:-translate-y-0.5 active:translate-y-0 cursor-pointer"
        >
          Hire Me
        </a>
      </div>

      <!-- Mobile Hamburger Button -->
      <button 
        @click="isMobileMenuOpen = !isMobileMenuOpen" 
        type="button" 
        class="md:hidden p-1.5 rounded-lg text-slate-400 hover:text-white hover:bg-slate-800/80 focus:outline-none transition-colors"
        aria-label="Toggle navigation"
      >
        <svg v-if="!isMobileMenuOpen" class="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24">
          <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16m-7 6h7" />
        </svg>
        <svg v-else class="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24">
          <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M6 18L18 6M6 6l12 12" />
        </svg>
      </button>
    </nav>

    <!-- Mobile Dropdown Menu -->
    <div 
      v-show="isMobileMenuOpen" 
      class="pointer-events-auto md:hidden mt-2 bg-slate-900/95 backdrop-blur-2xl border border-slate-800 shadow-2xl shadow-black/60 rounded-2xl p-4 space-y-1.5 transition-all"
    >
      <a 
        v-for="link in navLinks" 
        :key="link.name" 
        :href="link.href" 
        @click="scrollToSection($event, link.href)"
        class="block px-3.5 py-2.5 rounded-xl text-xs font-mono uppercase tracking-wider text-slate-300 hover:text-teal-300 hover:bg-slate-800/80 transition-colors"
      >
        {{ link.name }}
      </a>
      <a 
        href="#contact" 
        @click="scrollToSection($event, '#contact')"
        class="block w-full text-center text-xs font-mono uppercase tracking-wider font-bold px-4 py-3 rounded-xl bg-teal-400 hover:bg-teal-300 text-slate-950 transition-all shadow-md shadow-teal-500/20 mt-2"
      >
        Hire Me
      </a>
    </div>
  </header>
</template>