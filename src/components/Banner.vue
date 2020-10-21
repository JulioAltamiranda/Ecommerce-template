<template>
  <hooper  :infiniteScroll="true" progress="true" :autoPlay="false" :playSpeed="3000" :wheelControl="false">
    <slide>
      <div class="slide1" alt="slide1">
      </div>
      <div class="banner-text container">
        <p>Super Sale</p>
        <h2>Bluetooth 4.1 & Wireless</h2>
        <p>Lorem ipsum dolor, sit amet consectetur adipisicing elit. Quis eveniet nesciunt eius excepturi alias. Non iusto laborum excepturi ipsam accusantium?</p>
        <div class="banner-button">
          <a href="">Shop now</a>
          <i class="fas fa-caret-right"></i>
        </div>
      </div>
    </slide>
    <slide>
      <div class="slide2" alt="slide2">
      </div>
      <div class="banner-text container">
        <p>Super Sale</p>
        <h2>Win A Hitachi 49" Class 1080p LED</h2>
        <p>Lorem ipsum dolor, sit amet consectetur adipisicing elit. Quis eveniet nesciunt eius excepturi alias. Non iusto laborum excepturi ipsam accusantium?</p>
        <div class="banner-button">
          <a href="">Buy now</a>
          <i class="fas fa-caret-right"></i>
        </div>
      </div>
    </slide>
    <hooper-navigation slot="hooper-addons"></hooper-navigation>
  </hooper>
</template>
<script>
import {
  Hooper,
  Slide,
  Navigation as HooperNavigation,
  Pagination as HooperPagination
  } from 'hooper';
import 'hooper/dist/hooper.css';

export default {
  components: {
    Hooper,
    Slide,
    HooperNavigation,
    HooperPagination
  }
}
</script>