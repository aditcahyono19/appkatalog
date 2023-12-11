<template>
  <div class="row">
    <div class="col">
      <div class="d-flex h-100">
        <div class="justify-content-center align-self-center">
          <h2><strong>Delicious Food Menu,</strong><br />In Your Gedget</h2>
          <p>Ayo segera pilih dan pesan makanan favorit anda </p>
            <router-link class="btn btn-lg btn-success" to="/menu">Menu</router-link>
        </div>
      </div>
    </div>
    <div class="col">
      <img src="../assets/images/eating.png" width="100%" />
    </div>
  </div>
</template>

<script>
export default {
  // eslint-disable-next-line vue/multi-word-component-names
  name: "Hero",
};
</script>

<style>
</style>