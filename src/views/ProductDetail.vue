<template>
  <div>
    <NavBar />
    <div class="container">
      <div class="row mt-3">
        <div class="col-md-6">
          <img :src="detailProduct.product_img" class="img-fluid shadow" />
        </div>
        <div class="col-md-6">
          <h2 style="color: black">
            <strong>{{ detailProduct.product_name }}</strong>
          </h2>
          <hr />
          <h4 style="color: black">
            Harga :
            <strong>Rp. {{ detailProduct.product_price }}</strong>
          </h4>
          <hr />
          <h4 style="color: black">
            Stok Barang : <strong>{{ detailProduct.product_qty_stock }}</strong>
          </h4>
          <form class="mt-4">
            <div class="form-group">
              <label>Jumlah pemesanan</label>
              <input type="number" class="form-control" style="width: 120px;" />
            </div>
            <div>
              <label>Keterangan</label> <br>
              <label>{{ detailProduct.product_description }}</label>
            </div>
            <hr>
            <button type="submit" class="btn btn-success">
              <b-icon-cart></b-icon-cart>Pesan
            </button>
          </form>
        </div>
      </div>
    </div>
    <FooterView />
  </div>
</template>

<script>
import NavBar from "@/components/NavBar.vue";
import FooterView from "@/components/FooterView.vue";
import axios from "axios";

export default {
  name: "ProductDetail",
  components: {
    NavBar,
    FooterView,
  },
  data() {
    return {
      detailProduct: {},
    };
  },
  methods: {
    setProduct(data) {
      this.detailProduct = data;
    },
  },
  mounted() {
    axios
      .get("https://sistemtoko.com/public/demo/single/" + this.$route.params.id)
      .then((response) => {
        this.setProduct(response.data);
        console.log("berhasil", response.data);
      })
      .catch((error) => {
        console.log(error);
      });
  },
};
</script>

<style>
</style>