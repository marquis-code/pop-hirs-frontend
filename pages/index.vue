<template>
    <div class="relative min-h-screen  w-full overflow-hidden bg-white">
      <div class="hidden lg:absolute lg:inset-0 lg:block" aria-hidden="true">
        <svg class="absolute left-1/2 top-0 -translate-y-8 translate-x-64 transform" width="640" height="784" fill="none" viewBox="0 0 640 784">
          <defs>
            <pattern id="9ebea6f4-a1f5-4d96-8c4e-4c2abf658047" x="118" y="0" width="20" height="20" patternUnits="userSpaceOnUse">
              <rect x="0" y="0" width="4" height="4" class="text-gray-200" fill="currentColor" />
            </pattern>
          </defs>
          <rect y="72" width="640" height="640" class="text-gray-50" fill="currentColor" />
          <rect x="118" width="404" height="784" fill="url(#9ebea6f4-a1f5-4d96-8c4e-4c2abf658047)" />
        </svg>
      </div>
  
      <div class="relative pb-16 pt-6 sm:pb-24 lg:pb-32 h-screen">
        <div>
          <nav class="relative mx-auto flex max-w-7xl items-center justify-between px-6" aria-label="Global">
            <div class="flex flex-1 items-center">
              <div class="flex w-full items-center justify-between md:w-auto">
                <!-- <a href="#">
                  <span class="sr-only">Your Company</span>
                  <img class="h-16 w-auto sm:h-16" src="@/assets/img/pop-hirs-logo.png" alt="">
                </a> -->
                <div class="-mr-2 flex items-center md:hidden">
                  <button @click="toggle" type="button" class="relative inline-flex items-center justify-center rounded-md bg-white p-2 text-gray-400 hover:bg-gray-100 hover:text-gray-500 focus:outline-none focus:ring-2 focus:ring-inset focus:ring-indigo-500" aria-expanded="false">
                    <span class="absolute -inset-0.5"></span>
                    <span class="sr-only">Open main menu</span>
                    <svg class="h-6 w-6" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" aria-hidden="true">
                      <path stroke-linecap="round" stroke-linejoin="round" d="M3.75 6.75h16.5M3.75 12h16.5m-16.5 5.25h16.5" />
                    </svg>
                  </button>
                </div>
              </div>
              <div class="hidden md:ml-10 md:block md:space-x-10">
                <a href="#" class="font-medium text-gray-500 hover:text-gray-900">Product</a>
                <a href="#" class="font-medium text-gray-500 hover:text-gray-900">About Us</a>
                <a href="#" class="font-medium text-gray-500 hover:text-gray-900">Partnership</a>
                <a href="#" class="font-medium text-gray-500 hover:text-gray-900">Resources</a>
              </div>
            </div>
            <!-- <div class="hidden text-right md:block">
              <span class="inline-flex rounded-md shadow-md ring-1 ring-black ring-opacity-5">
                <a href="#" class="inline-flex items-center rounded-md border border-transparent bg-white px-4 py-2 text-base font-medium text-indigo-600 hover:bg-gray-50">Log in</a>
              </span>
            </div> -->
          </nav>
  
          <div v-if="isOpen" class="absolute inset-x-0 top-0 z-10 origin-top-right transform p-2 transition md:hidden">
            <div class="overflow-hidden rounded-lg bg-white shadow-md ring-1 ring-black ring-opacity-5">
              <div class="flex items-center justify-between px-5 pt-4">
                <!-- <div>
                  <img class="h-16 w-auto" src="@/assets/img/pop-hirs-logo.png" alt="">
                </div> -->
                <div class="-mr-2">
                  <button @click="toggle" type="button" class="relative inline-flex items-center justify-center rounded-md bg-white p-2 text-gray-400 hover:bg-gray-100 hover:text-gray-500 focus:outline-none focus:ring-2 focus:ring-inset focus:ring-indigo-500">
                    <span class="absolute -inset-0.5"></span>
                    <span class="sr-only">Close main menu</span>
                    <svg class="h-6 w-6" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" aria-hidden="true">
                      <path stroke-linecap="round" stroke-linejoin="round" d="M6 18L18 6M6 6l12 12" />
                    </svg>
                  </button>
                </div>
              </div>
              <div class="space-y-1 px-2 pb-3 pt-2">
                <a @click="toggle" href.prevent="#" class="block rounded-md px-3 py-2 text-base font-medium text-gray-700 hover:bg-gray-50 hover:text-gray-900">Product</a>
                <a @click="toggle" href.prevent="#" class="block rounded-md px-3 py-2 text-base font-medium text-gray-700 hover:bg-gray-50 hover:text-gray-900">About Us</a>
                <a @click="toggle" href.prevent="#" class="block rounded-md px-3 py-2 text-base font-medium text-gray-700 hover:bg-gray-50 hover:text-gray-900">Partnership</a>
                <a @click="toggle" href.prevent="#" class="block rounded-md px-3 py-2 text-base font-medium text-gray-700 hover:bg-gray-50 hover:text-gray-900">Resources</a>
              </div>
              <!-- <a  @click="toggle" href.prevent="#" class="block w-full bg-gray-50 px-5 py-3 text-center font-medium text-indigo-600 hover:bg-gray-100">Log in</a> -->
            </div>
          </div>
        </div>
  
        <main class="mx-auto mt-16 max-w-7xl px-4 px-6 sm:mt-24 lg:mt-32">
          <div class="lg:grid lg:grid-cols-12 lg:gap-8">
            <div class="sm:text-center md:mx-auto md:max-w-2xl lg:col-span-6 lg:text-left">
              <h1>
                <span class="mt-1 block text-4xl font-bold tracking-tight sm:text-5xl xl:text-6xl">
                  <span class="block text-gray-900">Everything HR.</span>
                  <span class="block text-indigo-600">One Platform.</span>
                </span>
              </h1>
              <p class="mt-3 text-base text-gray-500 sm:mt-5 sm:text-xl lg:text-lg xl:text-xl">Easy-to-use HR management software that simplifies all of your HR processes, from recruitment to exit.</p>
              <div class="mt-8 sm:mx-auto sm:max-w-lg sm:text-center lg:mx-0 lg:text-left">
                <NuxtLink to="/auth" class="flex w-full items-center justify-center gap-3 rounded-md bg-white px-3 py-3 text-sm font-semibold text-gray-900 shadow-sm ring-1 ring-inset ring-gray-300 hover:bg-gray-50 focus-visible:ring-transparent">
                  <svg class="h-5 w-5" viewBox="0 0 24 24" aria-hidden="true">
                    <path d="M12.0003 4.75C13.7703 4.75 15.3553 5.36002 16.6053 6.54998L20.0303 3.125C17.9502 1.19 15.2353 0 12.0003 0C7.31028 0 3.25527 2.69 1.28027 6.60998L5.27028 9.70498C6.21525 6.86002 8.87028 4.75 12.0003 4.75Z" fill="#EA4335" />
                    <path d="M23.49 12.275C23.49 11.49 23.415 10.73 23.3 10H12V14.51H18.47C18.18 15.99 17.34 17.25 16.08 18.1L19.945 21.1C22.2 19.01 23.49 15.92 23.49 12.275Z" fill="#4285F4" />
                    <path d="M5.26498 14.2949C5.02498 13.5699 4.88501 12.7999 4.88501 11.9999C4.88501 11.1999 5.01998 10.4299 5.26498 9.7049L1.275 6.60986C0.46 8.22986 0 10.0599 0 11.9999C0 13.9399 0.46 15.7699 1.28 17.3899L5.26498 14.2949Z" fill="#FBBC05" />
                    <path d="M12.0004 24.0001C15.2404 24.0001 17.9654 22.935 19.9454 21.095L16.0804 18.095C15.0054 18.82 13.6204 19.245 12.0004 19.245C8.8704 19.245 6.21537 17.135 5.2654 14.29L1.27539 17.385C3.25539 21.31 7.3104 24.0001 12.0004 24.0001Z" fill="#34A853" />
                  </svg>
                  <span class="text-sm font-semibold leading-6">Sign in with Google</span>
                </NuxtLink>
              </div>
            </div>
            <div class="relative mt-12 sm:mx-auto sm:max-w-lg lg:col-span-6 lg:mx-0 lg:mt-0 lg:flex lg:max-w-none lg:items-center">
              <svg class="absolute left-1/2 top-0 origin-top -translate-x-1/2 -translate-y-8 scale-75 transform sm:scale-100 lg:hidden" width="640" height="784" fill="none" viewBox="0 0 640 784" aria-hidden="true">
                <defs>
                  <pattern id="4f4f415c-a0e9-44c2-9601-6ded5a34a13e" x="118" y="0" width="20" height="20" patternUnits="userSpaceOnUse">
                    <rect x="0" y="0" width="4" height="4" class="text-gray-200" fill="currentColor" />
                  </pattern>
                </defs>
                <rect y="72" width="640" height="640" class="text-gray-50" fill="currentColor" />
                <rect x="118" width="404" height="784" fill="url(#4f4f415c-a0e9-44c2-9601-6ded5a34a13e)" />
              </svg>
              <div class="relative mx-auto w-full rounded-lg shadow-lg lg:max-w-md">
                <button type="button" class="relative block w-full overflow-hidden rounded-lg bg-white">
                  <span class="sr-only">Watch our video to learn more</span>
                  <img class="w-full" src="@/assets/img/hirs.webp" alt="">
                  <span class="absolute inset-0 flex h-full w-full items-center justify-center" aria-hidden="true">
                    <svg class="h-20 w-20 text-indigo-500" fill="currentColor" viewBox="0 0 84 84">
                      <circle opacity="0.9" cx="42" cy="42" r="42" fill="white" />
                      <path d="M55.5039 40.3359L37.1094 28.0729C35.7803 27.1869 34 28.1396 34 29.737V54.263C34 55.8604 35.7803 56.8131 37.1094 55.9271L55.5038 43.6641C56.6913 42.8725 56.6913 41.1275 55.5039 40.3359Z" />
                    </svg>
                  </span>
                </button>
              </div>
            </div>
          </div>
        </main>
      </div>
    </div>
  </template>

  <script setup lang="ts">
  const isOpen = ref(false)

  const toggle = () => {
    isOpen.value = !isOpen.value
  }
  </script>
  