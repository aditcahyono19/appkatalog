<template>
  <div class="hero">
    <!-- dekstop -->
    <div class="d-none d-md-block">
      <div class="row mt-4">
        <div class="col-md-6">
          <div class="d-flex h-100">
            <div class="justify-content-center align-self-center">
              <h2>
                <strong>Deliciuous Food Menu,</strong><br />In Your Gedget
              </h2>
              <p>Ayo segera pilih dan pesan makanan favorit anda</p>
              <router-link class="btn btn-lg btn-success" to="/menu"
                >Menu</router-link
              >
            </div>
          </div>
        </div>
        <div class="col-md-6">
          <img src="../assets/images/eating.png" width="100%" />
        </div>
      </div>
    </div>

    <!-- mobile -->
    <div class="d-sm-block d-md-none">
      <div class="row mt-4">
        <div class="col-md-6 mb-3">
          <img src="../assets/images/eating.png" width="100%" />
        </div>
        <div class="col-md-6">
          <div class="d-flex h-100">
            <div class="justify-content-center align-self-center">
              <h2>
                <strong>Deliciuous Food Menu,</strong><br />In Your Gedget
              </h2>
              <p>Ayo segera pilih dan pesan makanan favorit anda</p>
              <router-link class="btn btn-lg btn-success" to="/menu"
                >Menu</router-link
              >
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
  name: "Hero",
};
</script>

<style></style>
