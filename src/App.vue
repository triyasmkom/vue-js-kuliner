<template>
  <div id="app">
    <nav>
    </nav>
    <router-view/>
    <Footer_ />
  </div>
</template>

<script>
  import Footer_ from '@/components/Footer.vue'
  export default{
    components:{Footer_}
  }
</script>

