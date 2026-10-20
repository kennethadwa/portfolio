<script setup>
import { ref, onMounted, onUnmounted } from 'vue'
import profilePic from '../assets/profile.jpg'

// Array ng mga titles/roles para sa typing animation
const roles = [
  'Full-Stack Web Developer',
  'IT Specialist',
  'Laravel & Vue.js Engineer',
  'Database Architect'
]

const displayText = ref('')
let roleIndex = 0
let charIndex = 0
let isDeleting = false
let timeoutId = null

const typeEffect = () => {
  const currentRole = roles[roleIndex]
  
  if (isDeleting) {
    // Burahin ang karakter
    displayText.value = currentRole.substring(0, charIndex - 1)
    charIndex--
  } else {
    // Itype ang karakter
    displayText.value = currentRole.substring(0, charIndex + 1)
    charIndex++
  }

  // Bilis ng pag-type at pagbura (in ms)
  let typeSpeed = isDeleting ? 40 : 80

  if (!isDeleting && charIndex === currentRole.length) {
    // Kapag natapos na ang buong salita, mag-pause sandali bago burahin
    typeSpeed = 2000
    isDeleting = true
  } else if (isDeleting && charIndex === 0) {
    // Kapag nabura na nang tuluyan, lumipat sa susunod na role
    isDeleting = false
    roleIndex = (roleIndex + 1) % roles.length
    typeSpeed = 400
  }

  timeoutId = setTimeout(typeEffect, typeSpeed)
}

onMounted(() => {
  typeEffect()
})

onUnmounted(() => {
  if (timeoutId) clearTimeout(timeoutId)
})
</script>

<template>
  <section id="home" class="min-h-screen pt-32 pb-20 flex items-center justify-center px-6 relative overflow-hidden">
    
    <div class="max-w-6xl mx-auto w-full grid grid-cols-1 lg:grid-cols-12 gap-12 lg:gap-8 items-center relative z-10">
      
      <!-- Left Column: Bio & Calls to Action -->
      <div class="lg:col-span-7 text-center lg:text-left space-y-6">
        
        <!-- Animated Availability Status Badge -->
        <div class="inline-flex items-center gap-2.5 px-3.5 py-1.5 rounded-full bg-slate-900/80 border border-slate-800 text-xs font-mono font-medium text-slate-300 backdrop-blur-md shadow-sm">
          <span class="relative flex h-2 w-2">
            <span class="animate-ping absolute inline-flex h-full w-full rounded-full bg-teal-400 opacity-75"></span>
            <span class="relative inline-flex rounded-full h-2 w-2 bg-teal-400"></span>
          </span>
          <span>AVAILABLE FOR FULL-STACK & WEB ROLES</span>
        </div>

        <!-- Name & Headline (High Contrast Pure Light Palette) -->
        <div class="space-y-2">
          <p class="text-xs sm:text-sm font-mono font-semibold tracking-widest text-teal-400 uppercase">
            // HELLO, WORLD! I AM
          </p>
          <h1 class="text-4xl sm:text-5xl lg:text-6xl font-black text-white tracking-tight leading-[1.08]">
            John Kenneth Lorenzo Ortigueras
          </h1>
          
          <!-- Typing Animation Container -->
          <h2 class="text-lg sm:text-2xl font-mono font-bold text-slate-300 pt-1 flex items-center justify-center lg:justify-start min-h-[2rem]">
            <span class="text-teal-300">{{ displayText }}</span>
            <span class="animate-cursor-blink text-teal-400 ml-1 font-extrabold">|</span>
          </h2>
        </div>

        <!-- Professional Biography -->
        <p class="text-base sm:text-lg text-slate-300 leading-relaxed max-w-2xl font-normal">
          Graduate of <strong class="text-white font-semibold">Bachelor of Science in Information Technology (Major in Web Development)</strong> from <strong class="text-teal-300 font-semibold">National University Lipa</strong>. Focused on developing responsive, high-performance web systems utilizing <span class="text-slate-100 font-semibold">Laravel, Vue.js, Tailwind CSS, and MySQL</span>.
        </p>

        <!-- Location & Contact Strip with High-Contrast Themed Icons -->
        <div class="flex flex-wrap items-center justify-center lg:justify-start gap-4 sm:gap-6 text-xs sm:text-sm text-slate-300 pt-1">
          <!-- Animated Location Item -->
          <div class="flex items-center gap-2.5 group cursor-default">
            <span class="flex items-center justify-center w-7 h-7 rounded-lg bg-teal-500/10 border border-teal-500/20 text-teal-300 shadow-sm animate-pin-bounce">
              <svg class="w-4 h-4" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M17.657 16.657L13.414 20.9a1.998 1.998 0 01-2.827 0l-4.244-4.243a8 8 0 1111.314 0z" />
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M15 11a3 3 0 11-6 0 3 3 0 016 0z" />
              </svg>
            </span>
            <span class="font-medium text-slate-200">Lipa City, Batangas</span>
          </div>

          <span class="hidden sm:inline text-slate-700">•</span>

          <!-- Animated Email Item -->
          <div class="flex items-center gap-2.5 group">
            <span class="flex items-center justify-center w-7 h-7 rounded-lg bg-sky-500/10 border border-sky-500/20 text-sky-300 shadow-sm animate-mail-wiggle">
              <svg class="w-4 h-4" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 8l7.89 5.26a2 2 0 002.22 0L21 8M5 19h14a2 2 0 002-2V7a2 2 0 00-2-2H5a2 2 0 00-2 2v10a2 2 0 002 2z" />
              </svg>
            </span>
            <a href="mailto:kennetics1@gmail.com" class="font-medium text-slate-200 hover:text-teal-300 transition-colors">
              kennetics1@gmail.com
            </a>
          </div>
        </div>

        <!-- High-Contrast Action Buttons -->
        <div class="flex flex-col sm:flex-row items-center justify-center lg:justify-start gap-4 pt-4">
          <!-- Download CV Button -->
          <a 
            href="/JOHN_KENNETH_L_ORTIGUERAS_CV.pdf" 
            download="JOHN_KENNETH_L_ORTIGUERAS_CV.pdf"
            class="group w-full sm:w-auto inline-flex items-center justify-center gap-2.5 px-7 py-3.5 rounded-xl bg-teal-400 hover:bg-teal-300 text-slate-950 font-bold text-xs sm:text-sm font-mono tracking-wider transition-all shadow-lg shadow-teal-500/20 hover:shadow-teal-400/30 hover:-translate-y-0.5 active:translate-y-0"
          >
            <svg class="w-4 h-4 group-hover:translate-y-0.5 transition-transform" fill="none" stroke="currentColor" viewBox="0 0 24 24">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 16v1a3 3 0 003 3h10a3 3 0 003-3v-1m-4-4l-4 4m0 0l-4-4m4 4V4" />
            </svg>
            DOWNLOAD CV
          </a>

          <!-- Explore Projects Button -->
          <a 
            href="#projects" 
            class="w-full sm:w-auto inline-flex items-center justify-center gap-2 px-7 py-3.5 rounded-xl bg-slate-900/80 hover:bg-slate-800 text-slate-200 border border-slate-700/80 hover:border-slate-600 font-mono text-xs sm:text-sm tracking-wider font-semibold transition-all hover:-translate-y-0.5"
          >
            EXPLORE PROJECTS
          </a>
        </div>
      </div>

      <!-- Right Column: Profile Card with Aurora Glow Ring -->
      <div class="lg:col-span-5 flex justify-center">
        <div class="relative group">
          
          <!-- Aurora Matching Glow Halo Behind Portrait -->
          <div class="absolute -inset-2 rounded-3xl bg-gradient-to-tr from-teal-500/40 via-sky-500/40 to-indigo-500/40 opacity-60 blur-xl animate-spin-slow"></div>

          <!-- Profile Frame Styled for Soft Dark Canvas -->
          <div class="relative w-64 h-64 sm:w-72 sm:h-72 lg:w-80 lg:h-80 rounded-2xl bg-slate-900/90 p-2 shadow-2xl border border-slate-800/90 backdrop-blur-md">
            <div class="w-full h-full rounded-[14px] overflow-hidden bg-slate-950 relative">
              <img 
                :src="profilePic" 
                alt="John Kenneth Lorenzo Ortigueras" 
                class="w-full h-full object-cover object-center group-hover:scale-105 transition-transform duration-700"
              />
            </div>
          </div>

        </div>
      </div>

    </div>
  </section>
</template>

<style scoped>
/* Typing Cursor Blink Animation */
@keyframes cursor-blink {
  0%, 100% { opacity: 1; }
  50% { opacity: 0; }
}

.animate-cursor-blink {
  animation: cursor-blink 0.8s infinite;
}

/* Infinite Subtle Halo Spin */
@keyframes spin-slow {
  from { transform: rotate(0deg); }
  to { transform: rotate(360deg); }
}

/* Continuous Micro-Bouncing Location Pin */
@keyframes pin-bounce {
  0%, 100% {
    transform: translateY(0);
  }
  50% {
    transform: translateY(-4px);
  }
}

/* Continuous Subtle Mail Wiggle */
@keyframes mail-wiggle {
  0%, 100% {
    transform: rotate(0deg);
  }
  25% {
    transform: rotate(-6deg);
  }
  75% {
    transform: rotate(6deg);
  }
}

.animate-spin-slow {
  animation: spin-slow 24s linear infinite;
}

.animate-pin-bounce {
  animation: pin-bounce 2.2s ease-in-out infinite;
}

.animate-mail-wiggle {
  animation: mail-wiggle 3s ease-in-out infinite;
}
</style>