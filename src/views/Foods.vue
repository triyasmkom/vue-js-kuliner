<template>
  <div>
    <Navbar />
    <h2>Daftar Makanan</h2>
  </div>
</template>

<script>
  // @ is an alias to /src
  import Navbar from '@/components/Navbar.vue'
  export default {
      // eslint-disable-next-line vue/multi-word-component-names
      name: "Foods",

      components:{
        Navbar
      }
  }
</script>

<style>

</style>