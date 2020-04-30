<template>
  <div>
    <header class="site-header">
      <div class="site-branding">
        <h1 class="site-title">
          <a href="index.html" rel="home">
            <!-- <img src="images/logo.png" alt="Logo" /> -->
          </a>
        </h1>
      </div>

      <div class="hamburger-menu">
        <div class="menu-icon">
          <img src="../assets/menu-icon.png" alt="menu icon" v-on:click="openMenu" />
        </div>

        <div class="menu-close-icon">
          <img src="../assets/x.png" alt="menu close icon" />
        </div>
      </div>
    </header>

    <nav class="site-navigation flex flex-column justify-content-between">
      <div class="site-branding d-none d-lg-block">
        <h1 class="site-title">
          <!-- <div>logo</div> -->
          <a href="index.html" rel="home">
            <img src="images/logo2.png" alt="Logo" />
          </a>
        </h1>
      </div>

      <ul class="main-menu flex flex-column justify-content-center">
        <li class="current-menu-item">
          <router-link to="/">Home</router-link>
          <!-- <a href="index.html">Home</a> -->
        </li>
        <li>
          <a href="#">Portfolio</a>
        </li>
        <li>
          <a href="#">Blog</a>
        </li>
        <li>
          <router-link to="/about">About</router-link>
          <!-- <a href="#">About</a> -->
        </li>
        <li>
          <a href="#">Contact</a>
        </li>
      </ul>

      <div class="social-profiles">
        <ul class="flex justify-content-start justify-content-lg-center align-items-center">
          <li>
            <a href="#">
              <font-awesoome-icon icon="fa-facebook"></font-awesoome-icon>
              <i class="fa fa-facebook"></i>
            </a>
          </li>
          <li>
            <a href="#">
              <font-awesoome-icon icon="fa-instagram"></font-awesoome-icon>
              <i class="fa fa-instagram"></i>
            </a>
          </li>
          <li>
            <a href="#">
              <font-awesoome-icon icon="fa-twitter"></font-awesoome-icon>
              <i class="fa fa-twitter"></i>
            </a>
          </li>
          <li>
            <a href="#">
              <font-awesoome-icon icon="fa-pinterest"></font-awesoome-icon>
              <i class="fa fa-pinterest"></i>
            </a>
          </li>
        </ul>
      </div>
    </nav>
  </div>
</template>

<script>
import $ from "jquery";
export default {
  name: "Menu",
  props: {
    msg: String
  },

  methods: {
    openMenu() {
        $(this).toggleClass("close");
        $(".site-branding").toggleClass("hide");
        $(".site-navigation").toggleClass("show");
        $(".site-header").toggleClass("no-shadow");
    }
  }
};
</script>
<!-- Add "scoped" attribute to limit CSS to this component only -->
<style>
</style>
