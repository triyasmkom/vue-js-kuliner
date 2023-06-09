# Tutorial Vue Js

## Project setup
```
npm install
```

### Compiles and hot-reloads for development
```
npm run serve
```

### Compiles and minifies for production
```
npm run build
```

### Lints and fixes files
```
npm run lint
```

### Customize configuration
See [Configuration Reference](https://cli.vuejs.org/config/).


## Instalation
### Requirement
- Install node Js
- Install VS Code
- Inatall vue js : npm install -g @vue/cli
- Jalankan `vue ui` atau `vue ui -H 0.0.0.0 -p 8001`
    
    ![image](./image-readme/img2.png)

    Cara kerja vue ui Dibalik layar:

    ![image](./image-readme/img10.png)

### Buat Project melalui vue ui
#### 1. Setup nama project dan package manager 
![image](./image-readme/img3.png)
![image](./image-readme/img4.png)
![image](./image-readme/img1.png)
![image](./image-readme/img2.png)

#### 2. Install plugin

Plugin yang digunakan: router

![image](./image-readme/img5.png)
![image](./image-readme/img6.png)
![image](./image-readme/img7.png)


#### 3. Install depedensi

Depedensi yang digunakan: 

![image](./image-readme/img8.png)

![image](./image-readme/img9.png)


#### 4. Task

![image](./image-readme/11.png)

![image](./image-readme/12.png)


#### 5. Struktur Project

Struktur Project

![image](./image-readme/13.png)

File main.js: dari main, panggil app

![image](./image-readme/14.png)

File App.vue

![image](./image-readme/15.png)

Dari App vue memanggil router view

![image](./image-readme/16.png)

Router View

![image](./image-readme/17.png)

Dari router view memanggil `home` dan `about`.


![image](./image-readme/18.png)

Home

![image](./image-readme/19.png)

About

![image](./image-readme/20.png)


## Membuat Halaman Home

Kita bersihkan terlebih dahulu ```app.vue``` menjadi seperti ini:

![image](./image-readme/home1.png)

Kemudian kita membuat nav bar file (```Navbar.vue```) di folder components:

![image](./image-readme/home2.png)

![image](./image-readme/home3.png)

Ubah file ```HomeView.vue``` :

![image](./image-readme/home4.png)


![image](./image-readme/home5.png)


![image](./image-readme/home6.png)


Kita buat navbar dari ```bootstrap``` atau ```bootstrap-vue``` :
- bootstrap: https://getbootstrap.com/
- bootstrap-vue: https://bootstrap-vue.org/

Mari kita cari navbar dari bootstrap:

```vue
<nav class="navbar navbar-expand-lg bg-body-tertiary">
  <div class="container-fluid">
    <a class="navbar-brand" href="#">Navbar</a>
    <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
      <span class="navbar-toggler-icon"></span>
    </button>
    <div class="collapse navbar-collapse" id="navbarSupportedContent">
      <ul class="navbar-nav me-auto mb-2 mb-lg-0">
        <li class="nav-item">
          <a class="nav-link active" aria-current="page" href="#">Home</a>
        </li>
        <li class="nav-item">
          <a class="nav-link" href="#">Link</a>
        </li>
        <li class="nav-item dropdown">
          <a class="nav-link dropdown-toggle" href="#" role="button" data-bs-toggle="dropdown" aria-expanded="false">
            Dropdown
          </a>
          <ul class="dropdown-menu">
            <li><a class="dropdown-item" href="#">Action</a></li>
            <li><a class="dropdown-item" href="#">Another action</a></li>
            <li><hr class="dropdown-divider"></li>
            <li><a class="dropdown-item" href="#">Something else here</a></li>
          </ul>
        </li>
        <li class="nav-item">
          <a class="nav-link disabled">Disabled</a>
        </li>
      </ul>
      <form class="d-flex" role="search">
        <input class="form-control me-2" type="search" placeholder="Search" aria-label="Search">
        <button class="btn btn-outline-success" type="submit">Search</button>
      </form>
    </div>
  </div>
</nav>

```

![image](./image-readme/home7.png)

https://getbootstrap.com/docs/5.3/components/navbar/#how-it-works


Selanjutnya kita copy dan paste ke file ```Navbar.vue```:

```vue

<template>
  <nav class="navbar navbar-expand-lg bg-body-tertiary">
  <div class="container-fluid">
    <a class="navbar-brand" href="#">Navbar</a>
    <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
      <span class="navbar-toggler-icon"></span>
    </button>
    <div class="collapse navbar-collapse" id="navbarSupportedContent">
      <ul class="navbar-nav me-auto mb-2 mb-lg-0">
        <li class="nav-item">
          <a class="nav-link active" aria-current="page" href="#">Home</a>
        </li>
        <li class="nav-item">
          <a class="nav-link" href="#">Link</a>
        </li>
      </ul>
    </div>
  </div>
</nav>
</template>

<script>
export default {
    
    // eslint-disable-next-line vue/multi-word-component-names
    name: 'Navbar'
}
</script>

<style>

</style>

 ```

![image](./image-readme/home8.png)

Karena tampilannya masih seperti itu, mari kita lanjutkan konfigurasi bootstrap-vue. 

![image](./image-readme/home9.png)

```
import { BootstrapVue, BootstrapVueIcons } from 'bootstrap-vue'

import 'bootstrap/dist/css/bootstrap.css'
import 'bootstrap-vue/dist/bootstrap-vue.css'

Vue.use(BootstrapVue)
Vue.use(BootstrapVueIcons)

```

https://bootstrap-vue.org/docs


Kemudian paste di file ```main.js``` :

![image](./image-readme/home11.png)

![image](./image-readme/home10.png)


Mari kita lanjutkan mendesain tampilan home kita, file ```Navbar.vue``` :

```vue
<template>
  <nav class="navbar navbar-expand-lg bg-body-tertiary">
  <div class="container">
    <a class="navbar-brand" href="#">Kulineran</a>
    <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
      <span class="navbar-toggler-icon"></span>
    </button>
    <div class="collapse navbar-collapse" id="navbarSupportedContent">
      <ul class="navbar-nav me-auto mb-2 mb-lg-0">
        <li class="nav-item">
          <router-link class="nav-link" to="/">Home</router-link>
        </li>
        <li class="nav-item">
          <router-link class="nav-link" to="/foods">Foods</router-link>
        </li>
      </ul>
    </div>
  </div>
</nav>
</template>

<script>
export default {
    
    // eslint-disable-next-line vue/multi-word-component-names
    name: 'Navbar'
}
</script>

<style>

</style>

```

Kemudian kita buat views untuk ```Foods.vue``` :

![image](./image-readme/home12.png)

```vue
<template>
  <h2>Daftar Makanan</h2>
</template>

<script>
export default {
    // eslint-disable-next-line vue/multi-word-component-names
    name: "Foods"
}
</script>

<style>

</style>


```

Untuk file Foods.vue kita daftarkan ke router:

![image](./image-readme/home13.png)

![image](./image-readme/home14.png)

![image](./image-readme/home15.png)


Tambahkan navbar di file ```Foods.vue```:

```vue
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

```

![image](./image-readme/home16.png)



selanjutnya kita tambahkan keranjang di file ```Navbar.vue``` :

```vue
<template>
  <nav class="navbar navbar-expand-lg bg-body-tertiary">
    <div class="container">
      <a class="navbar-brand" href="#">Kulineran</a>
      <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
        <span class="navbar-toggler-icon"></span>
      </button>
      <div class="collapse navbar-collapse" id="navbarSupportedContent">
        <!-- Navbar Menu -->
        <ul class="navbar-nav mr-auto mb-2 mb-lg-0">
          <li class="nav-item">
            <router-link class="nav-link" to="/">Home</router-link>
          </li>
          <li class="nav-item">
            <router-link class="nav-link" to="/foods">Foods</router-link>
          </li>
        </ul>
        <!-- Keranjang -->
        <ul class="navbar-nav ml-auto mb-2 mb-lg-0">
          <li class="nav-item">
            <router-link class="nav-link" to="/keranjang">Keranjang</router-link>
          </li>
        </ul>
      </div>
    </div>
  </nav>
</template>

<script>
export default {
    
    // eslint-disable-next-line vue/multi-word-component-names
    name: 'Navbar'
}
</script>

<style>

</style>


```


![image](./image-readme/home17.png)

Kita tambahkan icon di keranjang, dimana icon dapat diambil dari bootstrap-vue https://bootstrap-vue.org/docs/icons :

![image](./image-readme/home18.png)

tinggal ambil saja dan paste ke sini:

![image](./image-readme/home20.png)

![image](./image-readme/home19.png)

Kita tambahkan span:

![image](./image-readme/home21.png)

![image](./image-readme/home22.png)

Desain css, kita buat file ```main.css``` di folder assets:

```css
.router-link-exact-active{
font-weight: bold;
}

```

dan kita load di file main.js :

![image](./image-readme/home23.png)


Mengganti font di https://fonts.google.com/specimen/Montserrat?query=mont:

![image](./image-readme/home24.png)

Kita embed dan kita taruh di public index.html:

![image](./image-readme/home25.png)

Selanjutnya kita implementasikan css-nya di main.css:

![image](./image-readme/home26.png)


Membuat banner, mari kita siapkan tampilannya di folder components:

file Hero.vue
```vue
<template>
  <div class="row">
    <div class="col">
        <h2><strong>Delicious Food Menu, </strong><br> in Your Gadged</h2>
    </div>

    <div class="col">

    </div>

  </div>
</template>

<script>
export default {
    // eslint-disable-next-line vue/multi-word-component-names
    name: 'Hero'
}
</script>

<style>

</style>

```


dan import ke file HomeView.vue:

```vue
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

```


membuat ilustrasi, pake undraw https://undraw.co/illustrations :

![image](./image-readme/home27.png)

Desain:

```
Warna Primary: #4EB883
Warna PrimSecondary: #E9F9F4
Ilustrasi: undraw.co
Gambar: unplash.com
Font: Montserrat
```

Setelah kita mencari gambar di ```undraw.co```, dan kita simpan di src/assets/images:

![image](./image-readme/home28.png)


Kita pasang gambarnya di ```Hero.vue```:


```vue
<template>
  <div class="row">
    <div class="col">
      <div class="d-flex h-100">
        <div class="justify-content-center align-self-center">
          <h2><strong>Delicious Food Menu, </strong><br> in Your Gadged</h2>
          <p>Ayo segera pilih dan pesan makanan faovorite Anda</p>
          <button class="btn btn-lg btn-success">Pesan  <b-icon-arrow-right></b-icon-arrow-right></button>
        </div>
      </div>
    </div>

    <div class="col">
      <img src="./../assets/images/hero.png" alt="" width="100%">
    </div>

  </div>
</template>

<script>
export default {
    // eslint-disable-next-line vue/multi-word-component-names
    name: 'Hero'
}
</script>

<style>

</style>

```

Tambahkan css di ```main.css```:

![image](./image-readme/home29.png)

![image](./image-readme/home30.png)



## Membuat Server Tiruan menggunakan Json-server

Dokumentasi: https://github.com/typicode/json-server

Pertama kita install terlebih dahulu:

```bash
npm install -g json-server
```

Buat file db.json untuk database backend kita:

```json
{
"best_products":[],
"products":[],
"keranjang":[],
"pesanan":[]
}

```

Jalankan server tiruan kita:

```bash
json-server -p 4000 --watch ./kuliner-be/db.json
```

![image](./image-readme/api1.png)


## Memnbuat Card Product

Pertama kita rapikan terlebih dahulu tampilannya antara mobile dan desktop di file ```Hero.vue``` :

```vue
<template>
  <div class="hero">
    <!-- Desktop -->
    <div class="d-none d-md-block">
      <div class="row mt-4">
        <div class="col-md-6">
          <div class="d-flex h-100">
            <div class="justify-content-center align-self-center">
              <h2><strong>Delicious Food Menu, </strong><br> in Your Gadged</h2>
              <p>Ayo segera pilih dan pesan makanan faovorite Anda</p>
              <button class="btn btn-lg btn-success">Pesan  <b-icon-arrow-right></b-icon-arrow-right></button>
            </div>
          </div>
        </div>

        <div class="col">
          <img src="./../assets/images/hero.png" alt="" width="100%">
        </div>
      </div>
    </div>

    <!-- Mobile -->
    <div class="d-sm-block d-md-none">
      <div class="row mt-4">
        <div class="col-md-6 mb-3">
          <img src="./../assets/images/hero.png" alt="" width="100%">
        </div>
        <div class="col-md-6">
          <div class="d-flex h-100">
            <div class="justify-content-center align-self-center">
              <h2><strong>Delicious Food Menu, </strong><br> in Your Gadged</h2>
              <p>Ayo segera pilih dan pesan makanan faovorite Anda</p>
              <button class="btn btn-lg btn-success">Pesan  <b-icon-arrow-right></b-icon-arrow-right></button>
            </div>
          </div>
        </div>
      </div>
    </div>

  </div>
  
</template>

<script>
export default {
    // eslint-disable-next-line vue/multi-word-component-names
    name: 'Hero'
}
</script>

<style>

</style>

```

![image](./image-readme/api2.png)

![image](./image-readme/api3.png)



Membuat tampilan best foods, buat component file ```CardProduct.vue``` :

![image](./image-readme/api4.png)


```vue
<template>
  <h2>Card Product {{ product.nama }}</h2>
</template>

<script>
export default {
    name: "CardProduct",
    props:['product']
}
</script>

<style>

</style>
```

Ubah di file ```HomeView.vue ```menjadi seperti ini:

![image](./image-readme/api5.png)

![image](./image-readme/api6.png)


```vue
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

```



![image](./image-readme/api7.png)

Sekarang kita gunakan bootstrap untuk membuat card:

```vue
<div class="card">
  <div class="card-body">
    This is some text within a card body.
  </div>
</div>

```

![image](./image-readme/api8.png)

Kita cari gambar sesuai dengan response dari API dan simpan di folder public:

![image](./image-readme/ap10.png)

Kemudian kita copy paste code dari bootstrap ke file CardProduct.vue menjadi seperti ini:

```vue
<template>
  <!-- <h2>Card Product {{ product.nama }}</h2> -->
  <div class="card" style="width: 18rem">
    <img :src="'./assets/images/'+product.gambar" class="card-img-top" alt="..." />
    <div class="card-body">
      <p class="card-text">
        Card Product {{ product.nama }}
      </p>
    </div>
  </div>
</template>

<script>
export default {
  name: "CardProduct",
  props: ["product"],
};
</script>

<style>
</style>

```

Membuat file untuk footer:

![image](./image-readme/api10.png)

```vue
<template>
  <footer class="mt-5 mb-5">
    <hr />
    <div class="container">
      <div class="row">
        <div class="col text-center">
            2023 © Triyas HS
        </div>
      </div>
    </div>
  </footer>
</template>

<script>
export default {
    name: "Footer_"
};
</script>

<style>
</style>

```

Kemudian kita panggil di App.vue :

```vue
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

```

dan main.css menjadi seperti ini:

```css
.router-link-exact-active{
font-weight: bold;
}

#app{
font-family: 'Montserrat', sans-serif;
font-family: 'Open Sans', sans-serif;
}

.btn-success{
background-color: #4EB883;
}

.badge-success{
background-color: #4EB883;
}

.card-product{
border-radius: 15px;
}

.card-img-top{
border-top-right-radius: 15px;
border-top-left-radius: 15px;
}

```