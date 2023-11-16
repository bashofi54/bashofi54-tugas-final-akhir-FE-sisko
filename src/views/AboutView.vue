<template>
  <div>
    <NavBar />
    <div class="about container" >
      <h1>This is an about page</h1>
    </div>
    <FooterView />
  </div>
</template>

<script>
// @ is an alias to /src
import NavBar from '@/components/NavBar.vue'
import FooterView from '@/components/FooterView.vue';

export default {
  name: 'HomeView',
  components: {
    NavBar,
    FooterView,
  }
}
</script>