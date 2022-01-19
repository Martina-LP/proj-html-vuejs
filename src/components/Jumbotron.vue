<template>
  <div>
    <div class="d-flex">
      <!-- Prev button -->
      <div class="prev position-absolute">
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

      <img :src="require('../assets/img/' + imgJ + '.png')" :alt="imgJ" class="jumbo">
      <img :src="require('../assets/img/' + imgJTwo + '.png')" :alt="imgJTwo" class="jumbo male">

      <img :src="require('../assets/img/' + leafOne + '.png')" :alt="leafOne" class="position-absolute leaf_one"> 
      <img :src="require('../assets/img/' + leafTwo + '.png')" :alt="leafTwo" class="position-absolute leaf_two">   
      <img :src="require('../assets/img/' + leafThree + '.png')" :alt="leafThree" class="position-absolute leaf_three">
      <img :src="require('../assets/img/' + leafFour + '.png')" :alt="leafFour" class="position-absolute leaf_four">
      <img :src="require('../assets/img/' + leafFour + '.png')" :alt="leafFour" class="position-absolute leaf_fourth">
      <img :src="require('../assets/img/' + leafFive + '.png')" :alt="leafFive" class="position-absolute leaf_five">

      <!-- Next button -->
      <div class="next position-absolute">
        <i class="fas fa-chevron-right"></i>
      </div>
      <!-- End next button -->
    </div>
    <!-- Lower dots -->
    <div class="d-flex justify-content-center">
      <div class="dots"></div>
      <div class="dots"></div>
      <div class="dots"></div>
    </div>
    <!-- End lower dots -->
  </div>
</template>

<script>
export default {
    name: "Jumbotron",

    props: {
      imgJ: Image,
      imgJTwo: Image,
      txtJ: String,
      txtSJ: String,
      captionJ: String,
      btnJ: String,
      leafOne: Image,
      leafTwo: Image,
      leafThree: Image,
      leafFour: Image,
      leafFive: Image

    },
  
}
</script>

<style scoped lang="scss">
@import "../style/general.scss";
@import "../style/colors.scss";

.first-text {
  font-size: 80px;
  padding: 100px 0 0 300px;
  line-height: 80px;
  font-weight: 200;
}

p {
  padding: 20px 30px 10px 300px;
  font-size: 20px;
  color: $gray;
}

.btn {
  margin-left: 300px;
  padding: 14px 30px;
  font-size: 14px;
  font-weight: bold;
  border: 3px solid $pink;
}

img {
  padding: 100px 0 40px 10px;
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
  left: 0;
  top: 400px;
}

.next {
  right: 0;
  top: 400px;
}

.prev:hover, .next:hover {
  transform: scale(1.2);
}

.jumbo {
  width: 40%;
}

.male {
  margin-right: 60px;
}

.leaf_one {
  bottom: 380px;
  right: 980px;
}

.leaf_two {
  bottom: 148px;
  right: 930px;
}

.leaf_three {
  bottom: 134px;
  right: 50px;
}

.leaf_four {
  top: 52px;
  right: 944px;
}

.leaf_fourth {
  transform: rotate(90deg);
  top: 218px;
  right: 42px;
}

.leaf_five {
  top: 18px;
  right: 142px;
}

.dots {
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
