<template>
  <div id="app">
    <div class="qode position-fixed p-2 shadow">
      <a href="#">
        <img src="./assets/img/svg/white-circle.svg" alt="White Circle" class="w-img">
      </a>
    </div>
    <div class="shop position-fixed p-2 shadow">
      <a href="#">
        <img src="./assets/img/svg/shopping-cart.svg" alt="Shopping Cart" class="w-shop">
      </a>
    </div>
    <div class="arrow-back position-fixed">
      <a href="#top">
        <img src="./assets/img/svg/arrow-up.svg" alt="Arrow Up" class="w-100">
      </a>
    </div>

    <Header />

    <main>
      <Main />
    </main>

    <Footer />
  </div>
</template>

<script>
import Header from "./components/Header.vue";
import Main from "./components/Main.vue";
import Footer from "./components/Footer.vue";

export default {
  name: "App",
  components: {
    Header,
    Main,
    Footer

  },

  data(){
    return {
      informations: [
        {
          
        }
      ]
    }
  }
};
</script>

<style lang="scss">
@import "../node_modules/bootstrap/scss/bootstrap.scss";
@import "./style/general.scss";
@import "./style/colors.scss";

#app {
  font-family: "Mulish", sans-serif;

  .qode {
    top: 170px;
    background-color: $red_bg;
  }

  .shop {
    top: 220px;
    background-color: $light;
    margin-left: 5px;
  }

  .qode, .shop {
    right: -80px;
    width: 10%;
    height: 4%;
    cursor: pointer;
    z-index: 1000;
  }

  .w-img {
    width: 13%;
  }

  .w-shop {
    width: 9%;
  }

  .arrow-back {
    background-color: $aqua_bg;
    width: 50px;
    height: 50px;
    bottom: 30px;
    right: 30px;
    padding: 15px;
    z-index: 1000;
  }
}
</style>
