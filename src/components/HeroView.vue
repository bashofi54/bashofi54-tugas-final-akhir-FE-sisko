<template>
  <div>
    <div class="carousel">
      <b-carousel
        id="carousel-1"
        v-model="slide"
        :interval="4000"
        background="#ababab"
        style="text-shadow: 1px 1px 2px #333"
      >
        <b-carousel-slide>
        <template #img>
          <img
            width="1110"
            height="300"
            src="https://t3.ftcdn.net/jpg/03/00/69/78/360_F_300697818_2hO5PJsuR9vH4WMeEuFVxr7Ad6U0d8EV.jpg"
            alt="image slot"
          >
        </template>
      </b-carousel-slide>
        <b-carousel-slide>
        <template #img>
          <img
            width="1110"
            height="300"
            src="https://i.pinimg.com/736x/b8/3f/6c/b83f6c2bb10b0bfe7cf4ab07e3e35b41.jpg"
            alt="image slot"
          >
        </template>
      </b-carousel-slide>
        <b-carousel-slide>
        <template #img>
          <img
            width="1110"
            height="300"
            src="https://i.pinimg.com/originals/b5/fc/e9/b5fce981d298bf989c295a5a4c091812.jpg"
            alt="image slot"
          >
        </template>
      </b-carousel-slide>
      </b-carousel>
    </div>
    <div class="row">
      <div class="col background-img">
        <h4>
          <strong>The Original Market Store,</strong><br />
          in your gadget
        </h4>
        <p>Segera pilih dan pesan fashion Anda..!!</p>
        <router-link class="btn btn-md btn-success" to="/product">
          <b-icon-arrow-right /> Pesan
        </router-link>
      </div>
      <div class="col bg-img"></div>
    </div>
    <div class="pic-offers-img">
      <a><img class="img-1" src="../assets/images/1.png" alt="" /></a>
      <a><img class="img-1" src="../assets/images/2.png" alt="" /></a>
      <a><img class="img-1" src="../assets/images/3.png" alt="" /></a>
      <a><img class="img-1" src="../assets/images/4.png" alt="" /></a>
    </div>
    <br />
    <div class="pic-grid-img-1">
      <a
        ><img
          class="img-1"
          height="500px"
          width="350px"
          src="../assets/images/5.jpg"
          alt=""
          srcset=""
      /></a>
      <a
        ><img
          class="img-1"
          height="500px"
          width="350px"
          src="../assets/images/6.jpg"
          alt=""
          srcset=""
      /></a>
      <a
        ><img
          class="img-1"
          height="500px"
          width="350px"
          src="../assets/images/7.jpg"
          alt=""
      /></a>
      <a><h4 class="info-of-img-below">For the Young, Wild & Stylish</h4></a>
      <a><h4 class="info-of-img-below">Just like your way to Conquer</h4></a>
      <a><h4 class="info-of-img-below">Stands out like the Sun</h4></a>
    </div>
    <br /><br />
    <div>
      <h2 class="head-of-offer">TRENDING NOW</h2>
      <p class="para-of-offer">From the runway to your wadrobe</p>
    </div>
    <br />
    <div class="index-grid-img-2">
      <a
        ><img class="img-1" src="../assets/images/12.jpg" id="trans-img" alt=""
      /></a>
      <a><img class="img-1" src="../assets/images/9.jpeg" alt="" /></a>
      <a><img class="img-1" src="../assets/images/10.jpg" alt="" /></a>
      <a
        ><img class="img-1" src="../assets/images/11.jpg" alt="" srcset=""
      /></a>
      <a
        ><img class="img-1" src="../assets/images/8.jpeg" alt="" srcset=""
      /></a>
      <a
        ><img class="img-1" src="../assets/images/13.webp" alt="" srcset=""
      /></a>
    </div>
    <br /><br />
    <div>
      <h2 class="head-of-offer">STYLES TO STEAL</h2>
      <p class="para-of-offer">Inspired by influencer</p>
    </div>
    <div class="index-grid-img-3">
      <a><img class="img-1" src="../assets/images/girl1.png" alt="" /></a>
      <a
        ><img class="img-1" src="../assets/images/girl2.png" alt="" srcset=""
      /></a>
      <a><img class="img-1" src="../assets/images/girl3.png" alt="" /></a>
      <a
        ><img class="img-1" src="../assets/images/girl4.png" alt="" srcset=""
      /></a>
    </div>
    <!-- ALL THE LINKS WILL GO TO products.html -->

    <br /><br />
  </div>
</template>

<script>
export default {
  name: "HeroView",
};
</script>

<style scoped>
.carousel {
  margin-top: 10px;
  margin-bottom: 10px;
}
.background-img {
  background-image: url("https://cloudfront-eu-central-1.images.arcpublishing.com/businessoffashion/BNS3JGFM2BBQ3MCBNLU3K4GO3E.jpg");
  background-size: cover;
  background-repeat: no-repeat;
  width: 300px;
  height: 400px;
  color: white;
  text-align: end;
  padding: 150px;
  margin-left: 15px;
}
.bg-img {
  background-image: url("../assets/images/Off-the-Wall.jpg");
  background-size: cover;
  background-repeat: no-repeat;
  margin-right: 15px;
}
.pic-offers-img {
  display: flex;
  grid-template-columns: repeat(4, 1fr);
  grid-gap: 8px;
  margin-top: 25px;
  overflow: hidden;
}
.img-1 {
  transform: scale(1);
  transition: all 0.3s ease-out;
}
.img-1:hover {
  transform: scale(1.1);
  transition: all 0.3s ease-in;
}
.pic-grid-img-1 {
  display: grid;
  grid-template-columns: 1fr 1fr 1fr;
  grid-gap: 30px;
  overflow: hidden;
}

.info-of-img-below {
  text-align: center;
  color: #ffffff;
  background-color: #f84258;
  padding-bottom: 5px;
}
.index-grid-img-2 {
  display: grid;
  grid-template-columns: 1fr 1fr 1fr;
  grid-gap: 20px;
  overflow: hidden;
  /* margin-left:20px; */
  /* margin-right: 20px; */
}

.index-grid-img-2 img:nth-child(3) {
  height: 220px;
  width: 355px;
  object-fit: cover;
}
.index-grid-img-2 img:nth-child(1) {
  height: 220px;
  width: 355px;
  object-fit: cover;
}
.index-grid-img-2 img:nth-child(4) {
  height: 220px;
  width: 355px;
  object-fit: cover;
}
.index-grid-img-2 img:nth-child(2) {
  height: 220px;
  width: 355px;
  object-fit: cover;
}
.index-grid-img-2 img:nth-child(5) {
  height: 220px;
  width: 355px;
  object-fit: cover;
}
.index-grid-img-2 img:nth-child(6) {
  height: 220px;
  width: 355px;
  object-fit: cover;
}
.head-of-offer {
  padding-left: 50px;
  color: black;
}
.para-of-offer {
  padding-left: 50px;
  color: black;
}
.index-grid-img-3 {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  grid-row-start: 1;
  grid-row-end: 3;
  overflow: hidden;
}
</style>