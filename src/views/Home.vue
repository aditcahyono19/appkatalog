<template>
  <div class="home">
    <Navbar />
    <div class="container">
      <Hero />

      <div class="row mt-4">
        <div class="col">
          <h2>Best<strong>Food</strong></h2>
        </div>
        <div class="col">
          <router-link to="/menu" class="btn btn-success float-right"
            ><b-icon-eye></b-icon-eye> Lihat Semua
          </router-link>
        </div>
      </div>

      <div class="row mb-3">
        <div class="col-md mt-4">
          <CardProducts />
        </div>
      </div>
    </div>
  </div>
</template>

<script>
// @ is an alias to /src
import Navbar from "@/components/Navbar.vue";
import Hero from "@/components/Hero.vue";
import CardProducts from "@/components/CardProducts.vue";
import axios from "axios";

export default {
  // eslint-disable-next-line vue/multi-word-component-names
  name: "Home",
  components: {
    Navbar,
    Hero,
    CardProducts,
  },
  data() {
    return {
      products: [],
    };
  },
  methods: {
    setProduct(data) {
      this.products = data;
    },
  },
  mounted() {
    axios
      .get("https://my-json-server.typicode.com/aditcahyono19/katalogmenu")
      .then(function (response) {
        console.log("berhasil : ",response);
      })
      .catch(function (error) {
        console.log("gagal : ",error);
      })
  },
};
</script>
