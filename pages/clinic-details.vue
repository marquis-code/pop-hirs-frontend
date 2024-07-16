<template>
    <div class="flex flex-col md:flex-row h-screen">
        <HospitalInfo class="flex-1" />
        <MapView class="flex-1" />
      </div>
  </template>  
  <style scoped>
  .container {
    display: flex;
    flex-direction: column;
    height: 100vh;
  }
  
  @media (min-width: 768px) {
    .container {
      flex-direction: row;
    }
  }
  
  .hospital-info, .map {
    flex: 1;
    height: 50%;
  }
  
  @media (min-width: 768px) {
    .hospital-info, .map {
      height: 100%;
    }
  }
  </style>
  