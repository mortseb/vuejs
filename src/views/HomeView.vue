<script setup>
import ButtonComponent from '../components/ButtonComponent.vue'
import TitleComponent from '../components/TitleComponent.vue'

</script>

<template>
  <main>
    <ButtonComponent text="Click Me" type="primary" @click="handleClick" />
    <ButtonComponent text="Danger" type="danger" />



    <TitleComponent text="h1 " type="h1" />
    <TitleComponent text="h2   " type="h2" />
    <TitleComponent text="h3   " type="h3" />
  </main>
</template>
