<template>
    <div @click="handleNavigation" class="bg-blue-100 border-2 border-blue-500 rounded-lg p-4 w-60 cursor-pointer">
      <div class="mb-2 w-60 space-y-4">
        <div class="">
            <span :class="statusClass" class="text-xs">{{ hospital.status }}</span>
        </div>
        <div class="">
            <h3 class="text-blue-700 max-w-[200px] font-semibold text-sm">{{ hospital.name }}</h3>
        </div>
      </div>
      <p class="text-gray-700 text-sm">{{ hospital.location }}</p>
    </div>
  </template>
  
  <script setup lang="ts">
  const router  = useRouter()
  const props = defineProps({
    hospital: {
        type: Object,
        required: true
      }
  })

  const statusClass = computed(() => {
        return props.hospital.status === 'Busy'
          ? 'bg-blue-600 text-white rounded-full px-2 py-1' : props.hospital.status === 'Unavailable' ? 'bg-red-600 text-white rounded-full px-2 py-1'
          : 'bg-green-600 text-white rounded-full px-2 py-1';
      });

      const handleNavigation = () => {
        router.push('/clinic-details')
      }
  </script>
  
  <style scoped>
  .status {
    display: inline-block;
    padding: 0.25rem 0.75rem;
    border-radius: 9999px;
  }
  </style>
  