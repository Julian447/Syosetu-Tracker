<script setup>
import { ref } from 'vue'
import { RouterView } from 'vue-router'
import Hamburger from './components/Hamburger.vue'

const menuOpen = ref(false)
</script>

<template>
  <div :class="{ 'menu-open': menuOpen }">
    <Hamburger @toggle="menuOpen = $event" />
    <div class="container">
      <RouterView/>
    </div>
  </div>
</template>

<style scoped>
.logo {
  height: 6em;
  padding: 1.5em;
  will-change: filter;
  transition: filter 300ms;
}
.logo:hover {
  filter: drop-shadow(0 0 2em #646cffaa);
}
.logo.vue:hover {
  filter: drop-shadow(0 0 2em #42b883aa);
}
</style>
