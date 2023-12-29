<template>
<div class="menu">
  <Navbar />
  <div class="container">
    <div class="row mt-4">
      <div class="col">
        <h2>Daftar <strong> Makanan </strong></h2>
      </div>
    </div>
    <div class="row mb-4">
        <div class="col-md-4 mt-4" v-for="product in products" :key="product.id">
          <CardProducts :product="product"/>
        </div>
      </div>
  </div>
</div>
</template>

<script>
import Navbar from "@/components/Navbar.vue";
import CardProducts from "@/components/CardProducts.vue";
import axios from "axios";
export default {
  // eslint-disable-next-line vue/multi-word-component-names
  name: "Menu",
  components: {
    Navbar,
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
    .get("http://localhost:3000/products")
    .then((response)=> this.setProduct(response.data))
    .catch((error)=>console.log(error))
  },
};
</script>

<style></style>
