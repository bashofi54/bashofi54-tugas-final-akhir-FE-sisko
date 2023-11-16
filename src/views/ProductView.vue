<template>
  <div>
    <NavBar />
    <div class="container">
      <div>
        <h2 class="main-head-of-products">
          Everyone Has A Style Statment<br />
          <span class="colored-word-bigger-size">FIND YOURS HERE!</span>
        </h2>
        <br />
        <div class="bg-images">
          <a href=""><img src="../assets/images/14.jpg" alt="" /></a>
        </div>
        <p class="msg-ps">
          <span class="colored-word">Click</span> on the product to add in your
          shopping list. <br />Go below and check
          <span class="colored-word">YOUR CART</span> for details.
        </p>
        <hr style="background-color: rgb(28, 162, 184); height: 2px" />
      </div>
      <div class="input-group mb-3">
        <input
        v-model="search"
        type="text"
        class="form-control"
        placeholder="Cari Produk"
        aria-label="Username"
        aria-describedby="basic-addon1"
        @keyup="searchProduct"
        />
        <span class="input-group-text" id="basic-addon1"><b-icon-search></b-icon-search></span>
      </div>
      <div class="row mb-4">
        <div
          class="col-md-3 mt-4"
          v-for="product in products"
          :key="product.id"
        >
          <CardProduct :product="product" />
        </div>
      </div>
    </div>
    <FooterView />
  </div>
</template>

<script>
// @ is an alias to /src
import NavBar from "@/components/NavBar.vue";
import CardProduct from "@/components/CardProduct.vue";
import FooterView from "@/components/FooterView.vue";
import axios from "axios";

export default {
  name: "ProductView",
  components: {
    NavBar,
    CardProduct,
    FooterView,
  },
  data() {
    return {
      products: [],
      search: '',
    };
  },
  methods: {
    setProduct(data) {
      this.products = data;
    },
    searchProduct() {
      axios
      .get("https://sistemtoko.com/public/demo/product?search_name="+this.search)
      .then((response) => {
        this.setProduct(response.data.aaData);
        // console.log("berhasil", response.data.aaData);
      })
      .catch((error) => {
        console.log(error);
      });
    }
  },
  mounted() {
    axios
      .get("https://sistemtoko.com/public/demo/product")
      .then((response) => {
        this.setProduct(response.data.aaData);
        console.log("berhasil", response.data.aaData);
      })
      .catch((error) => {
        console.log(error);
      });
  },
};
</script>

<style scoped>
.msg-ps {
  color: black;
  text-align: center;
  padding-bottom: 30px;
}
.bg-images {
  text-align: center;
  border-radius: 50px;
}
.bg-images img {
  width: 800px;
  object-fit: cover;
}
.bg-images {
  background-color: #f3f3f3;
}
.main-head-of-products {
  color: black;
  text-align: center;
}
.colored-word {
  color: #f84258;
}
.colored-word-bigger-size {
  color: #f84258;
  font-size: 35px;
}
</style>