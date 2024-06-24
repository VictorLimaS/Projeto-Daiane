<script setup>
  import Home from './pages/Home.vue'
</script>

<template>
  <div class="home">
    <Home/>
  </div>
</template>

<style scoped>
@media (max-width: 950px) {
  .home {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    }
}

</style>
