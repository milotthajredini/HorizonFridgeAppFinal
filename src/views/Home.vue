/*eslint-disable*/
<template>
  <div class="body">
    <div class="topBanner">
      <slider
        :touch="false"
        :control-btn="false"
        :indicators="false"
        animation="fade"
        style="height:100%"
        interval="4000"
        speed="200"
      >
        <slider-item>
          <img
            src="https://s3.eu-central-1.amazonaws.com/maia.horizon/Banners/CocaCola/test.png"
            alt=""
          />
        </slider-item>
        <slider-item>
          <img
            src="https://s3.eu-central-1.amazonaws.com/maia.horizon/Banners/CocaCola/2.png"
            alt=""
          />
        </slider-item>
      </slider>
    </div>
    <div class="drinks-row" style="padding:2% 0% 0% 0;height:218px">
      <Bottles />
    </div>

    <!-- <slider
        :touch="false"
        :control-btn="false"
        :indicators="false"
        animation="fade"
      >
        <slider-item>
          <img src="../assets/images/Banners/Pepsi/p.jpg" alt="" />
        </slider-item>
      </slider> -->

    <div class="drinks-row">
      <Bottles />
    </div>
    <!-- <div class="other-banners">
      <slider
        :touch="false"
        :control-btn="false"
        :indicators="false"
        animation="fade"
        style="height:100%;"
        interval="6000"
        speed="100"
      >
        <slider-item>
          <img src="../assets/images/Banners/Cocacola/50px.png" alt="" />
        </slider-item>
        <slider-item>
          <img src="../assets/images/Banners/Pepsi/p.jpg" alt="" />
        </slider-item>
      </slider>
    </div> -->
    <div class="drinks-row">
      <Cans />
    </div>

    <div class="drinks-row">
      <Pepsi />
    </div>
    <div class="drinks-row">
      <PepsiCans />
    </div>
    <div class="other-banners" style="height:8%">
      <slider
        :touch="false"
        :control-btn="false"
        :indicators="false"
        animation="fade"
        style="height:100%"
        interval="8000"
        speed="600"
      >
        <slider-item>
          <img
            src="https://s3.eu-central-1.amazonaws.com/maia.horizon/Banners/Pepsi/down.png"
            alt=""
          />
        </slider-item>
        <slider-item>
          <img
            src="https://s3.eu-central-1.amazonaws.com/maia.horizon/Banners/Pepsi/28.jpg"
            alt=""
          />
        </slider-item>
      </slider>
    </div>
  </div>
</template>
<script>
/*eslint-disable*/
import "../assets/css/Home.css";
import Bottles from "../components/Bottles.vue";
import Cans from "../components/Cans";
import Pepsi from "../components/Pepsi";
import PepsiCans from "../components/PepsiCans";
export default {
  components: {
    Bottles: Bottles,
    Cans: Cans,
    Pepsi: Pepsi,
    PepsiCans: PepsiCans
  }
};
</script>
