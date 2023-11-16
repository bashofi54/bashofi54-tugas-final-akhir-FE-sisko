<template>
  <div>
    <div class="card shadow" style="border-radius: 120px">
      <img
        :src="product.photo"
        style="border-top-left-radius: 15px; border-top-right-radius: 15px"
        alt="..."
      />
      <div class="card-body">
        <h5 class="card-title">
          {{ product.name }}
        </h5>
        <p class="card-text">Harga : Rp. {{ product.price }}</p>
        <router-link
          class="btn btn-border-none"
          style="
            padding-top: 0%;
            padding-bottom: 25px;
            color: rgb(28, 162, 184);
          "
          :to="'/product/' + product.id"
          ><b-icon-info-circle-fill></b-icon-info-circle-fill> Detail
          Product</router-link
        >
        <div class="button">
          <button
            type="button"
            class="btn btn-primary"
            id="show-btn"
            @click="$bvModal.show('modal-1' + product.id)"
          >
            <b-icon-cart></b-icon-cart> Pesan
          </button>
          <b-modal :id="'modal-1' + product.id" size="lg" :hide-header="true" :hide-footer="true">
            <div class="container">
              <div class="row mt-3">
                <div class="col-md-6">
                  <!-- <img :src="product.photo" class="img-fluid shadow" /> -->
                  <div>
                    <b-carousel
                      id="carousel-1"
                      v-model="slide"
                      :interval="4000"
                      controls
                      indicators
                      background="#ababab"
                      img-width="1024"
                      img-height="480"
                      style="text-shadow: 1px 1px 2px #333"
                      @sliding-start="onSlideStart"
                      @sliding-end="onSlideEnd"
                      ><b-carousel-slide
                        v-for="(photo, index) in product.photos"
                        :key="index"
                        :img-src="photo"
                      ></b-carousel-slide>
                    </b-carousel>
                  </div>
                </div>
                <div class="col-md-6">
                  <h2 style="color: black">
                    <strong>{{ product.name }}</strong>
                  </h2>
                  <hr />
                  <h4 style="color: black">
                    Harga :
                    <strong>Rp. {{ product.price }}</strong>
                  </h4>
                  <hr />
                  <h4 style="color: black">
                    Stok Barang :
                    <strong>{{ product.stock }}</strong>
                  </h4>
                  <form class="mt-4">
                    <div class="form-group">
                      <label>Jumlah pemesanan</label>
                      <input
                        type="number"
                        class="form-control"
                        style="width: 120px"
                      />
                    </div>
                    <div>
                      <label>Keterangan</label>
                      <label>{{ product.description }}</label>
                    </div>
                    <hr />
                    <button type="submit" class="btn btn-success">
                      <b-icon-cart></b-icon-cart>Pesan
                    </button>
                  </form>
                </div>
              </div>
            </div>
          </b-modal>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "CardProduct",
  props: ["product"],
};
</script>

<style>
.card-title {
  padding-left: 0%;
  color: black;
}
.card-text {
  padding-top: 0%;
  padding-left: 0%;
  color: black;
}
.button {
  text-align: center;
}
</style>