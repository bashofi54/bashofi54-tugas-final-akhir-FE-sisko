<template>
  <div class="home">
    <NavBar />
    <div class="container">
      <HeroView />
    </div>
    <FooterView/>
  </div>
</template>

<script>
// @ is an alias to /src
import NavBar from "@/components/NavBar.vue";
import HeroView from "@/components/HeroView.vue";
import FooterView from '@/components/FooterView.vue';

export default {
  name: "HomeView",
  components: {
    NavBar,
    HeroView,
    FooterView,
},
};
</script>
