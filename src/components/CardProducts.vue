<template>
<div class="card shadow">
  <img :src="'assets/images/' + product.gambar" class="card-img-top" alt="..."/>
  <div class="card-body">
    <h5 class="card-title">{{ product.nama }}</h5>
    <p class="card-text">Harga : Rp. {{ product.harga }}</p>
    <a href="#" class="btn btn-success"><b-icon-cart></b-icon-cart> Pesan </a>
  </div>
</div>
</template>

<script>
export default {
 name : 'CardProducts',
 props : ['product']
}
</script>

<style>

</style>