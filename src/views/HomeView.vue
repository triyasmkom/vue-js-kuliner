<template>
  <div class="home">
    <Navbar />
    <div class="container">
      <Hero/>
      <!-- menampilkan best foods -->
      <div class="row mt-4">
        <div class="col">
          <h2>Best <strong>Foods</strong></h2>
        </div>
        <div class="col">
          <router-link to="/foods" class="btn btn-success float-right"><b-icon-eye></b-icon-eye> Lihat semua</router-link>
        </div>
      </div>

      <div class="row mb-3">
        <div class="col-md-4 mt-4" v-for="product in products" :key="product.id">
          <CardProduct :product="product"/>
        </div>
      </div>

    </div>
  </div>
</template>

<script>
// @ is an alias to /src
import Navbar from '@/components/Navbar.vue'
import Hero from '@/components/Hero.vue'
import CardProduct from '@/components/CardProducts.vue'
import axios from 'axios'

export default {
  name: 'HomeView',
  // component yang ingin ditampilkan
  components: {
    Navbar, Hero, CardProduct
  },
  // untuk menampung data
  data(){
    return{
      products:[]
    }
  },
  // method untuk set data
  methods:{
    setProduct(data){
      this.products = data
    }
  },
  // menjalankan program yang ada di dalam mounted ketika halaman ini ditampilkan
  mounted(){
    axios.get("http://localhost:3000/products")
    // handle success
    .then((response)=>this.setProduct(response.data))
    // handle error
    .catch((error)=>console.log(error))
  }
}
</script>
