<template>
  <div>
<b-navbar toggleable="navbar navbar-expand-lg navbar-light bg-light">
  <div class="container">
    <a class="navbar-brand"><img src="../assets/images/icons8-plate-64.png" width="40px">   <strong>KATALOG</strong></a>
    <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>
    <b-collapse id="nav-collapse" is-nav>
      <b-navbar-nav>
        <li class="nav-item">
            <router-link class="nav-link" to="/">Home</router-link>
        </li>
        <li class="nav-item">
            <router-link class="nav-link" to="/menu">Menu</router-link>
        </li>
      </b-navbar-nav>
    </b-collapse>
        <ul class="navbar-nav ml-auto">
          <li class="nav-item">
            <router-link class="nav-link" to="/keranjang">Keranjang
              <b-icon-bag></b-icon-bag>
              <span class="badge badge-success ml-2">{{ jumlah_pesanans.length }}</span>
            </router-link>
          </li>
        </ul>
    </div>
</b-navbar>
</div>
</template>

<script>
import axios from "axios";
export default {
// eslint-disable-next-line vue/multi-word-component-names
name : 'Navbar',
data(){
return {
  jumlah_pesanans: []
}
},
methods: {
  setJumlah(data){
    this.jumlah_pesanans = data
  }
},
mounted (){
  axios
    .get("http://localhost:3000/keranjangs")
    .then((response)=> this.setJumlah(response.data))
    .catch((error)=>console.log(error))
}
};
</script>

<style>

</style>