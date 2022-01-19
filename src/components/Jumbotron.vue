<template>
  <div>
    <div class="d-flex">
      <!-- Prev button -->
      <div class="prev">
        <i class="fas fa-chevron-left"></i>
      </div>
      <!-- End prev button -->
      
      <div>
        <div class="first-text"> {{txtJ}} 
          <strong class="fst-italic fw-bold"> {{txtSJ}} </strong>
        </div>
        <p> {{captionJ}} </p>
        <button class="btn text-uppercase rounded-0">
          <span> {{btnJ}} </span>
        </button>   
      </div>

      <img :src="require('../assets/img/' + imgJ + '.png')" :alt="imgJ" class="w-75 jumbo">

      <img :src="require('../assets/img/' + leafOne + '.png')" :alt="leafOne" class="position-absolute leaf_one"> 
      <img :src="require('../assets/img/' + leafTwo + '.png')" :alt="leafTwo" class="position-absolute leaf_two">   
      <img :src="require('../assets/img/' + leafThree + '.png')" :alt="leafThree" class="position-absolute leaf_three">
      <img :src="require('../assets/img/' + leafFour + '.png')" :alt="leafFour" class="position-absolute leaf_four">
      <img :src="require('../assets/img/' + leafFour + '.png')" :alt="leafFour" class="position-absolute leaf_fourth">

      <!-- Next button -->
      <div class="next">
        <i class="fas fa-chevron-right"></i>
      </div>
      <!-- End next button -->
    </div>
    <!-- Lower dots -->
    <div class="d-flex justify-content-center">
      <div class="point"></div>
      <div class="point"></div>
      <div class="point"></div>
    </div>
    <!-- End lower dots -->
  </div>
</template>

<script>
export default {
    name: "Jumbotron",

    props: {
      imgJ: Image,
      txtJ: String,
      txtSJ: String,
      captionJ: String,
      btnJ: String,
      leafOne: Image,
      leafTwo: Image,
      leafThree: Image,
      leafFour: Image
    },
  
}
</script>

<style scoped lang="scss">
@import "../style/general.scss";
@import "../style/colors.scss";

.first-text {
  font-size: 80px;
  padding: 150px 50px 0 300px;
  line-height: 80px;
  font-weight: 200;
}

p {
  padding: 20px 30px 10px 300px;
  font-size: 20px;
  color: $gray;
}

.btn {
  margin-left: 308px;
  margin-right: 320px;
  padding: 14px 30px;
  font-size: 14px;
  font-weight: bold;
  border: 3px solid $pink;
}

img {
  margin-right: 80px;
  padding: 40px;
}

.prev, .next {
  font-size: 20px;
  color: $light;
  background-color: $pink;
  border-radius: 50%;
  padding: 0 10px 10px 10px;
  height: 30px;
  margin: 20px;
}

.prev {
  position: absolute;
  left: 0;
  top: 400px;
}

.next {
  position:absolute;
  right: 0;
  top: 400px;
}

.prev:hover, .next:hover {
  transform: scale(1.2);
}

.jumbo {
  padding: 20px;
}

.leaf_one {
  bottom: 236px;
  right: 800px;
}

.leaf_two {
  bottom: 160px;
  right: 720px;
}

.leaf_three {
  bottom: 180px;
  right: 85px;
}

.leaf_four {
  top: 212px;
  right: 800px;
}

.leaf_fourth {
  transform: rotate(90deg);
  top: 100px;
  right: 85px;
}

.point {
  content:"";
  width: 10px;
  height: 10px;
  border-radius: 50%;
  background-color: $pink;
  margin: 20px 10px;
  
  &:hover {
    transform: scale(1.2);
  }
}

button:hover {
  background-color: $pink;
  color: $light;
}

</style>
