<template>
    <div class="overflow-x-auto py-4 max-w-7xl mx-auto hide-scrollbar px-3 lg:px-0">
      <div class="flex space-x-4">
        <HospitalCard
          v-for="hospital in hospitals"
          :key="hospital.id"
          :hospital="hospital"
        />
      </div>
    </div>
  </template>
  
  <script lang="ts">
  import { defineComponent, ref } from 'vue';
  import HospitalCard from '@/components/HospitalCard.vue';
  
  export default defineComponent({
    name: 'HospitalsList',
    components: {
      HospitalCard
    },
    setup() {
      const hospitals = ref([
        {
          id: 1,
          name: 'Lagos University Teaching Hospital (LUTH)',
          location: 'Surulere',
          status: 'Busy'
        },
        {
          id: 2,
          name: 'Federal Medical College (FMC)',
          location: 'Yaba',
          status: 'Available'
        },
        {
          id: 1,
          name: 'Lagos University Teaching Hospital (LUTH)',
          location: 'Surulere',
          status: 'Busy'
        },
        {
          id: 2,
          name: 'Federal Medical College (FMC)',
          location: 'Yaba',
          status: 'Unavailable'
        },
        {
          id: 1,
          name: 'Lagos University Teaching Hospital (LUTH)',
          location: 'Surulere',
          status: 'Busy'
        },
        {
          id: 2,
          name: 'Federal Medical College (FMC)',
          location: 'Yaba',
          status: 'Unavailable'
        },
        {
          id: 1,
          name: 'Lagos University Teaching Hospital (LUTH)',
          location: 'Surulere',
          status: 'Busy'
        },
        {
          id: 2,
          name: 'Federal Medical College (FMC)',
          location: 'Yaba',
          status: 'Unavailable'
        },
        // Add more hospitals as needed
      ]);
  
      return {
        hospitals
      };
    }
  });
  </script>
  
  <style scoped>
  .hospital-card {
    min-width: 240px;
  }

  .hide-scrollbar {
    scrollbar-width: none; /* Firefox */
    -ms-overflow-style: none; /* IE 10+ */
  }
  .hide-scrollbar::-webkit-scrollbar {
    display: none; /* Chrome, Safari, Opera */
  }
  </style>
  