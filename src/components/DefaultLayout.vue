<template>
  <div class="bg-gray-100 h-full">
    <navbar />
    <main>
      <router-view />
    </main>
  </div>
</template>

<script setup>
import Navbar from "../components/Navbar.vue";
</script>

<script>
// You can leave this empty if you don't need to declare any additional logic or options
</script>
