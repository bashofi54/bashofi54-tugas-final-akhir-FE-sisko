<template>
  <div class="container">
    <b-navbar toggleable="lg" type="dark" variant="info">
      
      <b-collapse id="nav-collapse" is-nav>
        <b-navbar-nav>
          <router-link class="nav-link" to="/">Home</router-link>
          <router-link class="nav-link" to="/product">Products</router-link>
          <router-link class="nav-link" to="/about">About</router-link>
        </b-navbar-nav>
        <b-navbar-nav >
          <b-navbar-brand class="brand" href="/">FufuFashion</b-navbar-brand>
        </b-navbar-nav>
                <!-- Right aligned nav items -->
        <b-navbar-nav class="ml-auto">
          <b-navbar-nav>
            <router-link class="nav-link" to="/cart">Keranjang
              <b-icon-cart4></b-icon-cart4>
              <span class="badge badge-success ml-2">0</span>
            </router-link>
          </b-navbar-nav>
          <b-nav-item-dropdown right>
            <!-- Using 'button-content' slot -->
            <template #button-content>
              <em>User</em>
            </template>
            <b-dropdown-item href="#">Profile</b-dropdown-item>
            <b-dropdown-item href="#">Sign Out</b-dropdown-item>
          </b-nav-item-dropdown>
        </b-navbar-nav>
      </b-collapse>
    </b-navbar>
  </div>
</template>

<script>
export default {
  name: "NavBar",
};
</script>

<style scoped>
.brand {
  font-family: 'Condiment', cursive;
  margin-left: 135%;
  font-size: 250%;
  padding-bottom: 0%;
  padding-top: 0%;
}
.fff {
  text-align: center;
}
</style>
