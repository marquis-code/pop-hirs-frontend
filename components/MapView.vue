<template>
   <main class="relative">
    <div id="map" class="h-full w-full z-0"></div>
    <div class="absolute bottom-6 left-6 z-50">
        <HospitalInfoCard />
    </div>
   </main>
  </template>
  
  <script setup lang="ts">
  import { onMounted } from 'vue';
  import L from 'leaflet';
  
  onMounted(() => {
    const map = L.map('map').setView([6.5195, 3.3676], 15);
  
    L.tileLayer('https://{s}.tile.openstreetmap.org/{z}/{x}/{y}.png', {
      attribution: '© OpenStreetMap contributors'
    }).addTo(map);
  
    const pickup = [6.5195, 3.3676];
    const dropoff = [6.5244, 3.3792];
  
    L.circleMarker(pickup, { color: 'green' }).addTo(map);
    L.circleMarker(dropoff, { color: 'red' }).addTo(map);
  
    L.polyline([pickup, dropoff], { color: 'red' }).addTo(map);
  });
  </script>
  