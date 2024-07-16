   <template>
    <main class="relative h-full rounded-lg">
      <div id="map" class="h-full w-full z-0 rounded-lg"></div>
      <div class="absolute bottom-6 left-6 z-50 hidden lg:block">
        <HospitalInfoCard />
      </div>
    </main>
  </template>
  
  <script setup lang="ts">
  import { onMounted } from 'vue';
  import L from 'leaflet';
  
  onMounted(() => {
    const pickup = [6.5195, 3.3676];
    const dropoff = [6.5244, 3.3792];
  
    // Calculate the midpoint of the polyline
    const midpoint = [
      (pickup[0] + dropoff[0]) / 2,
      (pickup[1] + dropoff[1]) / 2,
    ];
  
    // Center the map around the midpoint
    const map = L.map('map').setView(midpoint, 15);
  
    L.tileLayer('https://{s}.tile.openstreetmap.org/{z}/{x}/{y}.png', {
      attribution: '© OpenStreetMap contributors',
    }).addTo(map);
  
    L.circleMarker(pickup, { color: 'green' }).addTo(map);
    L.circleMarker(dropoff, { color: 'red' }).addTo(map);
  
    L.polyline([pickup, dropoff], { color: 'red' }).addTo(map);
  });
  </script>
  
  <style scoped>
  /* Add any additional styles if needed */
  </style>
  