<template>
  <!-- Post -->
  <div class="position-relative">
    <div class="margin">
      <!-- Date -->
      <div class="box-position">
        <div class="box-top fst-italic fw-bold"> {{dayP}} </div>
        <div class="box-bottom text-uppercase"> {{monthP}} </div>
      </div>
      <!-- End date -->
      <!-- Picture -->
      <img :src="require('../assets/img/' + imgP + '.jpg')" :alt="imgP" class="w-100 box-img">
      <!-- End picture -->
    </div>
    <!-- Title and author -->
    <div class="h4 mt-3">
      <a href="#"> {{txtP}} </a>
    </div>
    <span class="fst-italic"> {{idP}} </span>
    <!-- End title and author -->
  </div>
  <!-- End post -->
</template>

<script>
export default {
    name: "Posters",
    props: {
      imgP: Image,
      txtP: String,
      idP: String,
      dayP: Number,
      monthP: String
    }
}
</script>

<style scoped lang="scss">
@import "../style/general.scss";
@import "../style/colors.scss";

.box-position {
  position:absolute;
  top: 130px;
  left: 30px;
  z-index: 96;
}

.box-top {
  width: 100%;
  padding: 4px 15px;
  font-size: 26px;
  background-color: $aqua_bg;
}

.box-bottom {
  width: 100%;
  height: 38px;
  padding: 3px 8px;
  font-size: 14px;
  background-color: $pink_bg;
  clip-path: polygon(0 0,100% 0,100% 100%,50% 70%,0 100%);
}

.margin {
  margin-top: 150px;
}

img {
  transition: transform 0.20s;

  &:hover {
    transform: scale(1.009);
  }
}

.h4 {
  font-size: 28px;

  a::after {
    content: "";
    position:absolute;
    width: 0;
    height: 6px;
    bottom: 60px;
    left: 10px;
    background-color: $aqua_bg;
    display: block;
    transition: width 1.5s;
  }

  a:hover::after {
    width: 90%;
  }
}
</style>
