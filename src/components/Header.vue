<template>
  <header>
    <div class="d-flex justify-content-between p-3">
      <!-- Logo -->
      <div class="p-2">
        <a href="#">
          <img src="../assets/img/logo-sidearea-1.png" alt="Logo">
        </a>
      </div>
      <!-- End Logo -->
      <!-- Nav -->
      <nav class="d-flex">
        <ul class="d-flex menu">
          <li v-for="(link, index) in links" :key="index" class="fw-bold m-3">
            <a :href="link.url" :class="{ 'current': link.current }">{{ link.text }}</a>
          </li>
        </ul>
        <div class="mx-2 p-1 mt-2">
          <a href="#"><img src="../assets/img/svg/grid-icon.svg" alt="Grid"></a>
        </div>
      </nav>
      <!-- End Nav -->
    </div>
    <div>
    <Jumbotron 
    v-for="(jb, index) in jumbos"
    :key="index"
    :imgJ="jb.imgJumbo"
    :txtJ="jb.textJumbo"
    :txtSJ="jb.textStrongJumbo"
    :btnJ="jb.buttonJumbo"
    :leafOne="jb.leafOne"
    :leafTwo="jb.leafTwo"
    :leafThree="jb.leafThree"
    :leafFour="jb.leafFour"
    />
    </div>
  </header>
</template>

<script>
import Jumbotron from './Jumbotron.vue';

export default {
  name: "Header",
  components: {
    Jumbotron,

  },

  data (){
    return {
      links : [
        {
          text: 'Home',
          url: '#',
          current: true,
        },
        {
          text: 'Pages',
          url: '#',
          current: false,
        },
        {
          text: 'Portfolio',
          url: '#',
          current: false,
        },
        {
          text: 'Blog',
          url: '#',
          current: false,
        },
        {
          text: 'Shop',
          url: '#',
          current: false,
        },
        {
          text: 'Elements',
          url: '#',
          current: false,
        },
      ],

      jumbos: [
        {
          imgJumbo: 'h-2-slider-img-15',
          textJumbo: 'Devotion that never',
          textStrongJumbo: 'ends',
          captionJumbo: 'Neque porro quisquam est, qui dolorem ipsum quia dolor sit amet, consectetur, adipisci velit, sed quia non numquam eius modi.',
          buttonJumbo: 'Read More',
          leafOne: 'h-2-slider-img-12',
          leafTwo: 'h-2-slider-img-13',
          leafThree: 'h-2-slider-img-14',
          leafFour: 'short-slider-rev-1-img-2'
        },
      ],
      
    }
  } 
}
</script>

<style scoped lang="scss">
@import "../style/general.scss";
@import "../style/colors.scss";

header {
  .menu {

    li {
      margin-left: 40px;
      font-size: 14px;
      list-style-type: none;

      a {
        display: inline-block;
        color: inherit;
        text-decoration: none;
        text-transform: uppercase;
        font-weight: bold;
        line-height: 10px;

        &.current {
          color: $dark;
          border-bottom: 4px solid $pink;
          line-height: 8px;
        }
      }
    }
  }
}
</style>
