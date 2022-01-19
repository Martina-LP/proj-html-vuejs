<template>
  <div>
    <div class="position-relative">
      <img :src="require('../assets/img/' + img + '.jpg')" :alt="img" class="w-100 image">
      <!-- Hover caption -->
      <div class="box">
        <a href="#" class="text">
          <p> {{txt}} </p>
        </a>
        <a href="#">
          <p class="fst-italic text-decoration-none"> {{id}} </p>
        </a>
      </div>
      <!-- End hover caption -->
    </div>
  </div>
</template>

<script>
export default {
  name: "Illustration",
  props: {
    img: Image,
    txt: String,
    id: String

  },

  data(){
    return {

    }
  }
}
</script>

<style scoped lang="scss">
@import "../style/general.scss";
@import "../style/colors.scss";

.box {
  position: absolute;
  width: 0%;
  top: 300px;
  left: 0;
  padding: 20px;
  background-color: $light;
  opacity: 0;
  transition: width .35s ease-in-out;
  z-index: 10;

  .text {
    font-size: 28px;
  }
}

.position-relative:hover > .box {
  width: 55%;
  opacity: 1;
}

</style>
