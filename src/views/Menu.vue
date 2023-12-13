<template>
  <div class="menu">
    <Navbar /><br />
    <div class="text-center">
      <h2><strong>MENU PENYETAN</strong></h2>
    </div>
    <br />
    <div class="container">
      <div>
        <b-card-group deck>
          <b-card
            title="Ayam Penyet"
            img-src="../assets/images/ayam-penyet.jpg"
            img-alt="Image"
            img-top
            tag="article"
            style="max-width: 20rem"
            class="mb-2"
          >
            <template #footer>
              <small class="text-muted">Rp. 16.000</small>
            </template>
          </b-card>

          <b-card
            title="Tempe Penyet"
            img-src="../assets/images/tempe-penyet.jpg"
            img-alt="Image"
            img-top
            tag="article"
            style="max-width: 20rem"
            class="mb-2"
          >
            <template #footer>
              <small class="text-muted">Rp. 10.000</small>
            </template>
          </b-card>

          <b-card
            title="Lele Penyet"
            img-src="../assets/images/lele-penyet.jpg"
            img-alt="Image"
            img-top
            tag="article"
            style="max-width: 20rem"
            class="mb-2"
          >
            <template #footer>
              <small class="text-muted">Rp. 13.000</small>
            </template>
          </b-card>
        </b-card-group>
      </div>
    </div>
  </div>
</template>

<script>
import Navbar from "@/components/Navbar.vue";
export default {
  // eslint-disable-next-line vue/multi-word-component-names
  name: "Menu",
  components: {
    Navbar,
  },
};
</script>

<style></style>
