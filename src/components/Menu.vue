<template>
  <div>
    <header class="site-header">
      <div class="site-branding">
        <h1 class="site-title">
          <a href="/" rel="home">
            <img src="../assets/navigation-icons/logo.png" alt="Logo" style="height:49px; width: 25px;" />
          </a>
        </h1>
      </div>

      <div class="hamburger-menu" v-on:click="openMenu">
        <div class="menu-icon">
          <img src="../assets/navigation-icons/menu-icon.png" alt="menu icon" />
        </div>

        <div class="menu-close-icon">
          <img src="../assets/navigation-icons/x.png" alt="menu close icon" />
        </div>
      </div>
    </header>

    <nav class="site-navigation flex flex-column justify-content-between">
      <div class="site-branding d-none d-lg-block">
        <h1 class="site-title"></h1>
      </div>

      <ul class="main-menu flex flex-column justify-content-center">
        <li class="current-menu-item" v-on:click="openMenu">
          <router-link to="/">Home</router-link>
        </li>
        <li v-on:click="openMenu">
          <router-link to="/portfolio">Portfolio</router-link>
        </li>
        <li v-on:click="openMenu">
          <router-link to="/blog">Blog</router-link>
        </li>
        <li v-on:click="openMenu">
          <router-link to="/about">About</router-link>
        </li>
        <li v-on:click="openMenu">
          <router-link to="/contact">Contact</router-link>
        </li>
      </ul>

      <div class="social-profiles">
        <ul class="flex justify-content-start justify-content-lg-center align-items-center">
          <li>
            <a href="https://www.facebook.com/justin.lu.18">
              <i>
                <img src="../assets/social-icons/001-facebook.svg" alt="alt" style="width:25px" />
              </i>
            </a>
          </li>
          <li>
            <a href="https://www.instagram.com/just_jlu/">
              <i>
                <img src="../assets/social-icons/011-instagram.svg" alt="alt" style="width:25px" />
              </i>
            </a>
          </li>
          <li>
            <a href="https://www.linkedin.com/in/justin-lu-b467ba99/">
              <i>
                <img src="../assets/social-icons/010-linkedin.svg" alt="alt" style="width:25px" />
              </i>
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
    openMenu: function() {
      $(this).toggleClass("close");
      $(".site-branding").toggleClass("hide");
      $(".site-navigation").toggleClass("show");
      $(".site-header").toggleClass("no-shadow");
      
    },
    linkClicked() {
      
    }
  }
};
</script>
<!-- Add "scoped" attribute to limit CSS to this component only -->

<style>
</style>
