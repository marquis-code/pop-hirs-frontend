
<template>
   <div class="px-2 lg:px-0">
    <div class="w-full max-w-7xl border border-gray-100 mx-auto rounded-lg p-2 bg-gray-50">
        <div class="bg-white shadow rounded-lg border border-gray-50 p-4 flex items-center">
          <div class="flex flex-col mr-4 w-1/2 border-r border-gray-100">
            <label class="text-gray-600 text-sm font-semibold flex items-center gap-x-2">
                <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="#417505" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><circle cx="11.5" cy="8.5" r="5.5"/><path d="M11.5 14v7"/></svg>
                Pick up location</label>
            <input type="text" v-model="pickupLocation" placeholder="Enter pickup location" class=" focus:outline-none focus:border-blue-500 text-xs py-3" />
          </div>
          <div class="flex flex-col mx-4 w-1/2 lg:border-r border-gray-100">
            <label class="text-gray-600 text-sm font-semibold flex items-center gap-x-2">
                <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="#4B0082" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><circle cx="12" cy="10" r="3"/><path d="M12 21.7C17.3 17 20 13 20 10a8 8 0 1 0-16 0c0 3 2.7 6.9 8 11.7z"/></svg>
                Destination location</label>
            <input type="text" v-model="destinationLocation" placeholder="Enter destination location" class=" focus:outline-none focus:border-blue-500 text-xs py-3" />
          </div>
          <div class="lg:flex flex-col mx-4 w-1/2 hidden">
            <label class="text-gray-600 text-sm font-semibold flex items-center gap-x-2">
                <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="#4a4a4a" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><circle cx="12" cy="12" r="10"></circle><polyline points="12 6 12 12 16 14"></polyline></svg>
                First trip</label>
            <input type="date" v-model="firstTripDate" class=" focus:outline-none focus:border-blue-500 text-xs py-3" />
          </div>
          <button @click="search" class="bg-black hidden text-white rounded-lg p-2 ml-4 lg:flex justify-center items-center">
            <svg xmlns="http://www.w3.org/2000/svg" width="19" height="19" viewBox="0 0 24 24" fill="none" stroke="#ffffff" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><circle cx="11" cy="11" r="8"></circle><line x1="21" y1="21" x2="16.65" y2="16.65"></line></svg>
          </button>
        </div>
      </div>
   </div>
  </template>
  
  <script setup lang="ts">
  import { ref } from 'vue'
  
  const pickupLocation = ref('')
  const destinationLocation = ref('')
  const firstTripDate = ref('')
  
  const search = () => {
    console.log('Searching for:', {
      pickupLocation: pickupLocation.value,
      destinationLocation: destinationLocation.value,
      firstTripDate: firstTripDate.value,
    })
  }
  </script>
  
  <style scoped>
  /* Add your custom styles here */
  </style>
  