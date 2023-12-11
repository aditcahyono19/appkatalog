<template>
  <div class="home">
   <Navbar />
   <div class="container">
    <Hero />
   </div>
  </div>
</template>

<script>
// @ is an alias to /src
import Navbar from '@/components/Navbar.vue'
import Hero from '@/components/Hero.vue'

export default {
  // eslint-disable-next-line vue/multi-word-component-names
  name: 'Home',
  components: {
    Navbar,
    Hero
  }
}
</script>
