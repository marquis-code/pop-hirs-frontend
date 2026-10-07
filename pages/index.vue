<template>
  <div class="min-h-screen bg-[#0B0F19] text-white font-sans selection:bg-indigo-500/30 selection:text-white relative overflow-hidden">
    <!-- Abstract Background -->
    <div class="absolute inset-0 z-0 overflow-hidden pointer-events-none">
      <div class="absolute -top-[20%] -left-[10%] w-[70%] h-[70%] rounded-full bg-indigo-900/40 blur-[120px] mix-blend-screen"></div>
      <div class="absolute top-[40%] -right-[10%] w-[60%] h-[60%] rounded-full bg-blue-900/30 blur-[100px] mix-blend-screen"></div>
      <div class="absolute -bottom-[20%] left-[20%] w-[50%] h-[50%] rounded-full bg-violet-900/30 blur-[100px] mix-blend-screen"></div>
      <!-- Subtle grid overlay -->
      <div class="absolute inset-0 bg-[url('data:image/svg+xml;base64,PHN2ZyB3aWR0aD0iNDAiIGhlaWdodD0iNDAiIHhtbG5zPSJodHRwOi8vd3d3LnczLm9yZy8yMDAwL3N2ZyI+CjxwYXRoIGQ9Ik0wIDBoNDB2NDBIMHoiIGZpbGw9Im5vbmUiLz4KPHBhdGggZD0iTTAgNDBoNDBWMEgweiIgZmlsbD0ibm9uZSIgc3Ryb2tlPSJyZ2JhKDI1NSwyNTUsMjU1LDAuMDMpIiBzdHJva2Utd2lkdGg9IjEiLz4KPC9zdmc+')] opacity-50"></div>
    </div>

    <!-- Navigation -->
    <nav class="fixed top-0 left-0 right-0 z-50 bg-[#0B0F19]/60 backdrop-blur-xl border-b border-white/5">
      <div class="max-w-7xl mx-auto px-6 h-20 flex items-center justify-between relative z-10">
        <div class="flex items-center gap-3">
          <div class="bg-white p-1.5 rounded-lg shadow-sm">
             <img src="@/assets/img/hayyiz-logo.jpg" alt="Hayyiz HRIS Logo" class="h-6 w-6 object-contain mix-blend-multiply" />
          </div>
          <span class="text-xl font-bold tracking-tight text-white">Hayyiz HRIS</span>
        </div>
        <div class="hidden md:flex items-center gap-8 text-sm font-medium text-slate-300">
          <a href="#features" class="hover:text-white transition-colors">Platform</a>
          <a href="#promotions" class="hover:text-white transition-colors">Promotions</a>
          <a href="#benefits" class="hover:text-white transition-colors">Benefits</a>
        </div>
      </div>
    </nav>

    <!-- Hero Section -->
    <main class="relative z-10 pt-40 pb-24 lg:pt-52 lg:pb-32 flex flex-col items-center text-center px-6">
      <div class="inline-flex items-center gap-2 px-4 py-2 rounded-full bg-white/5 border border-white/10 text-sm text-indigo-200 mb-8 backdrop-blur-md shadow-2xl">
        <span class="flex h-2 w-2 rounded-full bg-indigo-400 animate-pulse"></span>
        Authentic Human Resources
      </div>
      
      <h1 class="text-5xl md:text-7xl lg:text-[5.5rem] font-extrabold tracking-tight text-transparent bg-clip-text bg-gradient-to-br from-white via-indigo-100 to-indigo-400 mb-8 leading-[1.1] max-w-5xl">
        Elevate your team's <br class="hidden md:block"/> true potential.
      </h1>
      
      <p class="text-lg md:text-xl text-slate-300 leading-relaxed mb-12 max-w-2xl">
        The premium platform designed to track promotions, curate exclusive benefits, and cultivate a workplace culture built on authenticity.
      </p>

      <div class="flex justify-center">
        <NuxtLink to="/auth" class="group flex items-center justify-center gap-3 rounded-xl bg-white px-6 py-4 text-base font-semibold text-slate-900 shadow-[0_0_40px_-10px_rgba(255,255,255,0.3)] hover:shadow-[0_0_60px_-15px_rgba(255,255,255,0.5)] hover:-translate-y-1 transition-all duration-300">
          <svg class="h-6 w-6" viewBox="0 0 24 24" aria-hidden="true">
            <path d="M12.0003 4.75C13.7703 4.75 15.3553 5.36002 16.6053 6.54998L20.0303 3.125C17.9502 1.19 15.2353 0 12.0003 0C7.31028 0 3.25527 2.69 1.28027 6.60998L5.27028 9.70498C6.21525 6.86002 8.87028 4.75 12.0003 4.75Z" fill="#EA4335" />
            <path d="M23.49 12.275C23.49 11.49 23.415 10.73 23.3 10H12V14.51H18.47C18.18 15.99 17.34 17.25 16.08 18.1L19.945 21.1C22.2 19.01 23.49 15.92 23.49 12.275Z" fill="#4285F4" />
            <path d="M5.26498 14.2949C5.02498 13.5699 4.88501 12.7999 4.88501 11.9999C4.88501 11.1999 5.01998 10.4299 5.26498 9.7049L1.275 6.60986C0.46 8.22986 0 10.0599 0 11.9999C0 13.9399 0.46 15.7699 1.28 17.3899L5.26498 14.2949Z" fill="#FBBC05" />
            <path d="M12.0004 24.0001C15.2404 24.0001 17.9654 22.935 19.9454 21.095L16.0804 18.095C15.0054 18.82 13.6204 19.245 12.0004 19.245C8.8704 19.245 6.21537 17.135 5.2654 14.29L1.27539 17.385C3.25539 21.31 7.3104 24.0001 12.0004 24.0001Z" fill="#34A853" />
          </svg>
          Sign in with Google
        </NuxtLink>
      </div>
      
      <!-- App Preview -->
      <div class="max-w-6xl mx-auto mt-24 relative w-full">
        <div class="absolute -inset-1 bg-gradient-to-b from-indigo-500/30 to-transparent rounded-[2rem] blur-xl opacity-50"></div>
        <div class="relative rounded-[2rem] border border-white/10 bg-[#0B0F19]/50 backdrop-blur-xl p-3 shadow-2xl overflow-hidden">
          <div class="absolute inset-0 bg-gradient-to-t from-[#0B0F19] via-transparent to-transparent z-10 h-full w-full opacity-60"></div>
          <img src="@/assets/img/hirs.webp" alt="Hayyiz HRIS Dashboard" class="rounded-[1.5rem] w-full object-cover border border-white/5 opacity-80" />
        </div>
      </div>
    </main>
  </div>
</template>

<script setup lang="ts">
import { useHead } from '#app'

useHead({
  title: 'Hayyiz HRIS | Elevate Your Team',
})
</script>

<style>
html {
  scroll-behavior: smooth;
  background-color: #0B0F19;
}
</style>