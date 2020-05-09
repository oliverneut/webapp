<template>
  <div id="app">
    <Navbar />
    <ContentPage />
    
  </div>
</template>

<script>
  import Navbar from './components/Navbar.vue'
  import ContentPage from './components/ContentPage.vue'

  export default {
    name: 'app',
    components: {
      Navbar,
      ContentPage
    }
  }

</script>

<style>

</style>
