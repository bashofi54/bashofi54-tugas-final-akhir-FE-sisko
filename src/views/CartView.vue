<template>
  <div>
    <NavBar />
    <div class="container" >
      <h3>Keranjang belum tersedia</h3>
    </div>
    <FooterView />
  </div>
</template>

<script>
// @ is an alias to /src
import NavBar from '@/components/NavBar.vue'
import FooterView from '@/components/FooterView.vue';

export default {
  name: 'CartView',
  components: {
    NavBar,
    FooterView,
  }
}
</script>