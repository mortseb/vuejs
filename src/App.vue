<script setup>
import NavbarComponent from './components/NavbarComponent.vue'



</script>

<template class="dark">
  <header>
    <link rel="stylesheet"
      href="https://fonts.googleapis.com/css2?family=Material+Symbols+Outlined:opsz,wght,FILL,GRAD@24,400,0,0" />
  </header>
  <main>
    <NavbarComponent></NavbarComponent>
    <RouterView />
  </main>
</template>
