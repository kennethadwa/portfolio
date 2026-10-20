<script setup>
import Navbar from './components/Navbar.vue'
import Hero from './components/Hero.vue'
</script>

<template>
  <div class="min-h-screen bg-[#070b14] text-slate-200 font-sans selection:bg-sky-500 selection:text-white relative overflow-x-hidden scroll-smooth">
    
    <!-- ================= LIVE ANIMATED OCEANIC AURORA BACKGROUND ================= -->
    <div class="fixed inset-0 pointer-events-none z-0 overflow-hidden">
      
      <!-- Primary Oceanic Aurora Curtain (Cyan -> Sky Blue -> Deep Royal Blue -> Teal) -->
      <div class="aurora-curtain-primary absolute -top-[15%] -left-[20%] w-[140%] h-[75%] opacity-40 filter blur-[90px] mix-blend-screen pointer-events-none"></div>

      <!-- Secondary Counter-Flowing Aurora Beam (Electric Cobalt -> Azure -> Cyan) -->
      <div class="aurora-curtain-secondary absolute top-[25%] -right-[20%] w-[130%] h-[65%] opacity-30 filter blur-[110px] mix-blend-screen pointer-events-none"></div>

      <!-- Ambient Deep Glow Horizon (Deep Navy & Electric Teal) -->
      <div class="aurora-curtain-tertiary absolute -bottom-[10%] left-[5%] w-[110%] h-[55%] opacity-25 filter blur-[120px] mix-blend-screen pointer-events-none"></div>

      <!-- Subtle Dot Matrix Tech Layer for Eye-Pleasing Texture -->
      <div class="absolute inset-0 bg-dot-matrix opacity-20"></div>
    </div>

    <!-- Navigation Header -->
    <Navbar />

    <!-- Main Content Container -->
    <main class="relative z-10">
      
      <!-- 1. Hero Section -->
      <Hero />

      <!-- 2. About Me Section -->
      <section id="about" class="py-28 border-t border-slate-800/80 max-w-6xl mx-auto px-6">
        <div class="space-y-4 mb-14">
          <div class="inline-flex items-center gap-2 px-3 py-1 rounded-full bg-sky-500/10 border border-sky-500/20 text-sky-300 text-xs font-mono tracking-wider uppercase">
            // OVERVIEW
          </div>
          <h2 class="text-3xl sm:text-5xl font-black text-white tracking-tight">About Me</h2>
          <p class="text-slate-400 max-w-2xl text-base leading-relaxed font-normal">
            A software engineer specializing in scalable full-stack web applications, combining backend architectural integrity with modern, intuitive frontend interfaces.
          </p>
        </div>

        <!-- Metric Highlight Cards -->
        <div class="grid grid-cols-1 md:grid-cols-3 gap-6">
          <div class="p-7 rounded-2xl bg-slate-900/60 border border-slate-800 backdrop-blur-md hover:border-sky-500/40 transition-all duration-300 group">
            <div class="w-10 h-10 rounded-xl bg-sky-500/10 border border-sky-500/20 flex items-center justify-center text-sky-400 mb-5 group-hover:scale-110 transition-transform">
              <svg class="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 14l9-5-9-5-9 5 9 5z"/><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 14l6.16-3.422a12.083 12.083 0 01.665 6.479A11.952 11.952 0 0012 20.055a11.952 11.952 0 00-6.824-2.998 12.078 12.078 0 01.665-6.479L12 14z"/></svg>
            </div>
            <h3 class="text-lg font-bold text-white mb-2">NU Lipa Graduate</h3>
            <p class="text-slate-400 text-sm leading-relaxed">BS Information Technology, Major in Web Development (Class of 2026).</p>
          </div>

          <div class="p-7 rounded-2xl bg-slate-900/60 border border-slate-800 backdrop-blur-md hover:border-blue-500/40 transition-all duration-300 group">
            <div class="w-10 h-10 rounded-xl bg-blue-500/10 border border-blue-500/20 flex items-center justify-center text-blue-400 mb-5 group-hover:scale-110 transition-transform">
              <svg class="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M10 20l4-16m4 4l4 4-4 4M6 16l-4-4 4-4"/></svg>
            </div>
            <h3 class="text-lg font-bold text-white mb-2">Full-Stack Architecture</h3>
            <p class="text-slate-400 text-sm leading-relaxed">Proficient in building clean SPA and monolithic architectures using Laravel, Vue.js, Tailwind CSS, and MySQL.</p>
          </div>

          <div class="p-7 rounded-2xl bg-slate-900/60 border border-slate-800 backdrop-blur-md hover:border-teal-500/40 transition-all duration-300 group">
            <div class="w-10 h-10 rounded-xl bg-teal-500/10 border border-teal-500/20 flex items-center justify-center text-teal-400 mb-5 group-hover:scale-110 transition-transform">
              <svg class="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 12l2 2 4-4m5.618-4.016A11.955 11.955 0 0112 2.944a11.955 11.955 0 01-8.618 3.04A12.02 12.02 0 003 9c0 5.591 3.824 10.29 9 11.622 5.176-1.332 9-6.03 9-11.622 0-1.042-.133-2.052-.382-3.016z"/></svg>
            </div>
            <h3 class="text-lg font-bold text-white mb-2">Production-Tested</h3>
            <p class="text-slate-400 text-sm leading-relaxed">Engineered secure platforms deployed and adopted in live institutional and commercial environments.</p>
          </div>
        </div>
      </section>

      <!-- 3. Skills Section -->
      <section id="skills" class="py-28 border-t border-slate-800/80 max-w-6xl mx-auto px-6">
        <div class="space-y-4 mb-14">
          <div class="inline-flex items-center gap-2 px-3 py-1 rounded-full bg-teal-500/10 border border-teal-500/20 text-teal-300 text-xs font-mono tracking-wider uppercase">
            // CAPABILITIES
          </div>
          <h2 class="text-3xl sm:text-5xl font-black text-white tracking-tight">Technical Proficiency</h2>
          <p class="text-slate-400 max-w-2xl text-base leading-relaxed">Core technologies, frameworks, and developer environments utilized across production platforms.</p>
        </div>

        <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-6">
          <!-- Backend -->
          <div class="p-6 rounded-2xl bg-slate-900/60 border border-slate-800/90 backdrop-blur-md hover:border-slate-700 transition-all">
            <h3 class="text-xs font-mono font-bold uppercase tracking-wider text-sky-400 mb-4">// Backend & DB</h3>
            <div class="flex flex-wrap gap-2">
              <span v-for="skill in ['PHP', 'Laravel Framework', 'MySQL', 'Relational Schemas', 'RESTful APIs']" :key="skill" class="px-2.5 py-1 rounded-md bg-slate-800/70 text-slate-300 text-xs font-mono border border-slate-700/60">
                {{ skill }}
              </span>
            </div>
          </div>

          <!-- Frontend -->
          <div class="p-6 rounded-2xl bg-slate-900/60 border border-slate-800/90 backdrop-blur-md hover:border-slate-700 transition-all">
            <h3 class="text-xs font-mono font-bold uppercase tracking-wider text-blue-400 mb-4">// Frontend</h3>
            <div class="flex flex-wrap gap-2">
              <span v-for="skill in ['Vue.js 3', 'Tailwind CSS', 'JavaScript (ES6+)', 'HTML5', 'CSS3']" :key="skill" class="px-2.5 py-1 rounded-md bg-slate-800/70 text-slate-300 text-xs font-mono border border-slate-700/60">
                {{ skill }}
              </span>
            </div>
          </div>

          <!-- Environment -->
          <div class="p-6 rounded-2xl bg-slate-900/60 border border-slate-800/90 backdrop-blur-md hover:border-slate-700 transition-all">
            <h3 class="text-xs font-mono font-bold uppercase tracking-wider text-teal-400 mb-4">// Environment & Dev</h3>
            <div class="flex flex-wrap gap-2">
              <span v-for="skill in ['Vite', 'Laragon Local Dev', 'Git / GitHub', 'VS Code', 'Troubleshooting']" :key="skill" class="px-2.5 py-1 rounded-md bg-slate-800/70 text-slate-300 text-xs font-mono border border-slate-700/60">
                {{ skill }}
              </span>
            </div>
          </div>

          <!-- Tools -->
          <div class="p-6 rounded-2xl bg-slate-900/60 border border-slate-800/90 backdrop-blur-md hover:border-slate-700 transition-all">
            <h3 class="text-xs font-mono font-bold uppercase tracking-wider text-cyan-400 mb-4">// Design & Operations</h3>
            <div class="flex flex-wrap gap-2">
              <span v-for="skill in ['Figma', 'Canva', 'CapCut', 'Office Suites', 'Local SEO']" :key="skill" class="px-2.5 py-1 rounded-md bg-slate-800/70 text-slate-300 text-xs font-mono border border-slate-700/60">
                {{ skill }}
              </span>
            </div>
          </div>
        </div>
      </section>

      <!-- 4. Featured Projects Section -->
      <section id="projects" class="py-28 border-t border-slate-800/80 max-w-6xl mx-auto px-6">
        <div class="space-y-4 mb-14">
          <div class="inline-flex items-center gap-2 px-3 py-1 rounded-full bg-cyan-500/10 border border-cyan-500/20 text-cyan-300 text-xs font-mono tracking-wider uppercase">
            // PORTFOLIO
          </div>
          <h2 class="text-3xl sm:text-5xl font-black text-white tracking-tight">Featured Engineering Projects</h2>
          <p class="text-slate-400 max-w-2xl text-base leading-relaxed">Key systems designed, engineered, and shipped for enterprise and institutional clients.</p>
        </div>

        <div class="grid grid-cols-1 lg:grid-cols-2 gap-8">
          <!-- Project 1: NU DROP -->
          <div class="group relative rounded-2xl bg-slate-900/60 border border-slate-800 p-8 hover:border-sky-500/50 transition-all duration-300 flex flex-col justify-between">
            <div>
              <div class="flex items-center justify-between gap-4 mb-4">
                <span class="text-xs font-mono px-3 py-1 rounded-full bg-sky-500/10 text-sky-300 border border-sky-500/20">Production System</span>
                <span class="text-xs text-slate-500 font-mono">Lead Architect</span>
              </div>
              <h3 class="text-2xl font-bold text-white mb-3 group-hover:text-sky-300 transition-colors">
                NU DROP: Document Request & Online Payment System
              </h3>
              <p class="text-slate-400 text-sm leading-relaxed mb-6 font-normal">
                Official web application adopted and deployed by National University Lipa to streamline student document requests, robust user authentication, and campus online payment processing.
              </p>
            </div>
            <div>
              <div class="flex flex-wrap gap-2 pt-4 border-t border-slate-800">
                <span class="text-xs font-mono text-slate-400 px-2.5 py-1 rounded bg-slate-800/80 border border-slate-700/60">Laravel</span>
                <span class="text-xs font-mono text-slate-400 px-2.5 py-1 rounded bg-slate-800/80 border border-slate-700/60">Vue.js</span>
                <span class="text-xs font-mono text-slate-400 px-2.5 py-1 rounded bg-slate-800/80 border border-slate-700/60">Tailwind CSS</span>
                <span class="text-xs font-mono text-slate-400 px-2.5 py-1 rounded bg-slate-800/80 border border-slate-700/60">MySQL</span>
              </div>
            </div>
          </div>

          <!-- Project 2: SG Dental Clinic -->
          <div class="group relative rounded-2xl bg-slate-900/60 border border-slate-800 p-8 hover:border-blue-500/50 transition-all duration-300 flex flex-col justify-between">
            <div>
              <div class="flex items-center justify-between gap-4 mb-4">
                <span class="text-xs font-mono px-3 py-1 rounded-full bg-blue-500/10 text-blue-300 border border-blue-500/20">Healthcare Platform</span>
                <span class="text-xs text-slate-500 font-mono">Web Developer</span>
              </div>
              <h3 class="text-2xl font-bold text-white mb-3 group-hover:text-blue-300 transition-colors">
                SG Dental Clinic Booking & Management System
              </h3>
              <p class="text-slate-400 text-sm leading-relaxed mb-6 font-normal">
                Patient appointment and booking web application engineered with user-friendly frontend interfaces and relational MySQL database schemas for secure clinic record management.
              </p>
            </div>
            <div>
              <div class="flex flex-wrap gap-2 pt-4 border-t border-slate-800">
                <span class="text-xs font-mono text-slate-400 px-2.5 py-1 rounded bg-slate-800/80 border border-slate-700/60">Laravel</span>
                <span class="text-xs font-mono text-slate-400 px-2.5 py-1 rounded bg-slate-800/80 border border-slate-700/60">Tailwind CSS</span>
                <span class="text-xs font-mono text-slate-400 px-2.5 py-1 rounded bg-slate-800/80 border border-slate-700/60">MySQL</span>
                <span class="text-xs font-mono text-slate-400 px-2.5 py-1 rounded bg-slate-800/80 border border-slate-700/60">JavaScript</span>
              </div>
            </div>
          </div>
        </div>
      </section>

      <!-- 5. Experience Section -->
      <section id="experience" class="py-28 border-t border-slate-800/80 max-w-6xl mx-auto px-6">
        <div class="space-y-4 mb-14">
          <div class="inline-flex items-center gap-2 px-3 py-1 rounded-full bg-sky-500/10 border border-sky-500/20 text-sky-300 text-xs font-mono tracking-wider uppercase">
            // CAREER
          </div>
          <h2 class="text-3xl sm:text-5xl font-black text-white tracking-tight">Work Experience</h2>
        </div>

        <div class="space-y-8 relative before:absolute before:inset-0 before:left-3.5 before:w-0.5 before:bg-slate-800">
          <!-- Role 1 -->
          <div class="relative flex items-start gap-6 pl-10 group">
            <span class="absolute left-2 top-2 w-3.5 h-3.5 rounded-full bg-[#070b14] border-2 border-sky-400 group-hover:scale-125 transition-transform shadow-sm"></span>
            <div class="p-7 rounded-2xl bg-slate-900/60 border border-slate-800 w-full hover:border-slate-700 transition-all">
              <div class="flex flex-col sm:flex-row sm:items-center justify-between gap-1 mb-2">
                <h3 class="text-lg font-bold text-white">Marketing Specialist, Manager & Web Developer</h3>
                <span class="text-xs font-mono text-slate-400">June 2026 – September 2026</span>
              </div>
              <p class="text-sky-400 text-sm font-medium mb-3">RAJA Marketing Consultancy Services</p>
              <p class="text-slate-400 text-sm leading-relaxed font-normal">
                Architected and deployed responsive inventory browsing SPAs for property acquisitions, directed local SEO business indexing, and managed corporate cash and treasury operations.
              </p>
            </div>
          </div>

          <!-- Role 2 -->
          <div class="relative flex items-start gap-6 pl-10 group">
            <span class="absolute left-2 top-2 w-3.5 h-3.5 rounded-full bg-[#070b14] border-2 border-teal-400 group-hover:scale-125 transition-transform shadow-sm"></span>
            <div class="p-7 rounded-2xl bg-slate-900/60 border border-slate-800 w-full hover:border-slate-700 transition-all">
              <div class="flex flex-col sm:flex-row sm:items-center justify-between gap-1 mb-2">
                <h3 class="text-lg font-bold text-white">Web Developer (Intern)</h3>
                <span class="text-xs font-mono text-slate-400">March 2026 – May 2026</span>
              </div>
              <p class="text-teal-400 text-sm font-medium mb-3">SG Dental Clinic</p>
              <p class="text-slate-400 text-sm leading-relaxed font-normal">
                Engineered front-end interfaces using Tailwind CSS and developed back-end logic with Laravel and MySQL database management to process patient appointment requests.
              </p>
            </div>
          </div>
        </div>
      </section>

      <!-- 6. Contact Section -->
      <section id="contact" class="py-28 border-t border-slate-800/80 max-w-6xl mx-auto px-6">
        <div class="relative rounded-3xl bg-slate-900/80 border border-slate-800 p-8 sm:p-14 text-center overflow-hidden">
          <div class="relative z-10 max-w-2xl mx-auto space-y-6">
            <span class="text-xs font-mono px-3.5 py-1.5 rounded-full bg-sky-500/10 text-sky-300 border border-sky-500/20 uppercase tracking-wider">
              // CONNECT
            </span>
            <h2 class="text-3xl sm:text-5xl font-black text-white tracking-tight">
              Let's Build Scalable Systems
            </h2>
            <p class="text-slate-400 text-sm sm:text-base leading-relaxed font-normal">
              Available for full-time engineering appointments, contract development, and technical consulting.
            </p>

            <div class="pt-4 flex flex-col sm:flex-row items-center justify-center gap-4">
              <a 
                href="mailto:kennetics1@gmail.com" 
                class="w-full sm:w-auto inline-flex items-center justify-center gap-2 px-8 py-4 rounded-xl bg-sky-400 hover:bg-sky-300 text-slate-950 font-mono text-xs uppercase tracking-wider font-bold transition-all shadow-lg shadow-sky-500/20 hover:-translate-y-0.5"
              >
                Send an Email
              </a>
              <a 
                href="/JOHN_KENNETH_L_ORTIGUERAS_CV.pdf" 
                download="JOHN_KENNETH_L_ORTIGUERAS_CV.pdf"
                class="w-full sm:w-auto inline-flex items-center justify-center gap-2 px-8 py-4 rounded-xl bg-slate-800/80 hover:bg-slate-800 text-slate-200 border border-slate-700 font-mono text-xs uppercase tracking-wider font-bold transition-all hover:-translate-y-0.5"
              >
                Download CV
              </a>
            </div>
          </div>
        </div>
      </section>

    </main>

    <!-- Clean Dark Footer -->
    <footer class="py-12 border-t border-slate-800/80 text-center text-xs text-slate-500 relative z-10 bg-[#070b14]/80 backdrop-blur-sm font-mono">
      <div class="max-w-6xl mx-auto px-6 flex flex-col sm:flex-row items-center justify-between gap-4">
        <span>© {{ new Date().getFullYear() }} John Kenneth Lorenzo Ortigueras. All rights reserved.</span>
        <span class="text-slate-500">Vue 3 • Tailwind CSS • Vite</span>
      </div>
    </footer>

  </div>
</template>

<style scoped>
/* Dot Matrix Pattern Overlay */
.bg-dot-matrix {
  background-image: radial-gradient(rgba(148, 163, 184, 0.15) 1px, transparent 1px);
  background-size: 24px 24px;
}

/* ================= AURORA BOREALIS LIVE KEYFRAMES (PURE OCEAN BLUE PALETTE) ================= */

/* Primary Aurora Ribbon (Teal -> Cyan -> Sky Blue -> Deep Royal Blue) */
.aurora-curtain-primary {
  background: linear-gradient(
    115deg,
    rgba(14, 165, 233, 0.45),
    rgba(6, 182, 212, 0.4),
    rgba(37, 99, 235, 0.45),
    rgba(2, 132, 199, 0.4),
    rgba(20, 184, 166, 0.4)
  );
  background-size: 300% 300%;
  animation: aurora-flow-1 22s ease-in-out infinite alternate, aurora-blue-shift 26s linear infinite;
}

/* Secondary Counter-Flowing Aurora Ribbon (Cobalt -> Sky Blue -> Deep Cyan) */
.aurora-curtain-secondary {
  background: linear-gradient(
    -65deg,
    rgba(29, 78, 216, 0.35),
    rgba(56, 189, 248, 0.4),
    rgba(6, 182, 212, 0.35),
    rgba(30, 64, 175, 0.3)
  );
  background-size: 250% 250%;
  animation: aurora-flow-2 28s ease-in-out infinite alternate, aurora-blue-shift 32s linear infinite reverse;
}

/* Tertiary Horizon Glow (Navy -> Electric Blue -> Teal) */
.aurora-curtain-tertiary {
  background: linear-gradient(
    90deg,
    rgba(30, 58, 138, 0.35),
    rgba(14, 165, 233, 0.35),
    rgba(20, 184, 166, 0.3)
  );
  background-size: 200% 200%;
  animation: aurora-flow-3 18s ease-in-out infinite alternate;
}

/* Undulating Wave Motions */
@keyframes aurora-flow-1 {
  0% {
    transform: translateY(-8%) translateX(-5%) rotate(-2deg) scaleY(1);
    background-position: 0% 50%;
  }
  50% {
    transform: translateY(6%) translateX(4%) rotate(3deg) scaleY(1.18);
    background-position: 100% 50%;
  }
  100% {
    transform: translateY(-4%) translateX(2%) rotate(-1deg) scaleY(0.95);
    background-position: 50% 100%;
  }
}

@keyframes aurora-flow-2 {
  0% {
    transform: translateY(8%) translateX(6%) rotate(2deg) scale(1);
    background-position: 100% 0%;
  }
  50% {
    transform: translateY(-6%) translateX(-4%) rotate(-3deg) scale(1.12);
    background-position: 0% 100%;
  }
  100% {
    transform: translateY(4%) translateX(-2%) rotate(1deg) scale(0.98);
    background-position: 70% 50%;
  }
}

@keyframes aurora-flow-3 {
  0% {
    transform: translateY(4%) scaleX(1);
  }
  100% {
    transform: translateY(-6%) scaleX(1.15);
  }
}

/* Controlled Blue-Spectrum Color Cycle (Prevents shifting into purple) */
@keyframes aurora-blue-shift {
  0% {
    filter: blur(90px) hue-rotate(0deg);
  }
  50% {
    filter: blur(105px) hue-rotate(25deg);
  }
  100% {
    filter: blur(90px) hue-rotate(-20deg);
  }
}
</style>