<script setup>
import Navbar from "./components/NavbarComponent.vue";
import Footer from "./components/FooterComponent.vue";
</script>

<template>
  <div class="flex flex-col min-h-screen bg-gray-100">
    <Navbar />
    <div class="main max-width">
      <router-view></router-view>
    </div>
    <Footer />
  </div>
</template>
