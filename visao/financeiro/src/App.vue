<script setup>
  import { RouterView } from 'vue-router';
  import HeaderComponent from './components/Header.vue';
</script>

<template> 
  <div class="app-container">
    <HeaderComponent/>
    <RouterView/>
  </div>
</template>

<style scoped>
  .app-container{
    margin: 0;
    background-color: #1E1E1E;
    min-height: 100vh;
    color: white;
  }
</style>
