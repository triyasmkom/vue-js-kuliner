<template>
  <div class="home">
    <Navbar />
    <div class="container">
      <Hero/>
    </div>
  </div>
</template>

<script>
// @ is an alias to /src
import Navbar from '@/components/Navbar.vue'
import Hero from '@/components/Hero.vue'

export default {
  name: 'HomeView',
  components: {
    Navbar, Hero
  }
}
</script>
