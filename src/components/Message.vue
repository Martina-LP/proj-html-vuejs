<template>
  <div class="bg-image">
    <div class="container text-center">
      <!-- Title -->
      <div class="txt">Want to work with us? Send us <strong class="fst-italic">a message!</strong>
      </div>
      <!-- End title -->
      <!-- Description -->
      <p class="mt-2">Lorem ipsum dolor sit amet consectetur adipisicing elit. Inventore pariatur, nemo dolor, porro accusantium, aut autem esse doloremque repellendus beatae repellat exercitationem quibusdam qui labore dolores possimus saepe at iusto.</p>
      <!-- End description -->
      <!-- Contact button -->
      <button class="btn text-uppercase rounded-0"><span>Contact</span></button>
      <!-- End contact button -->
    </div>
  </div>
</template>

<script>
export default {
  name: "Message",

}
</script>

<style scoped lang="scss">
@import "../style/general.scss";
@import "../style/colors.scss";

.bg-image {
  background-image: url('../assets/img/rbt-placeholder.jpg');
  background-repeat: no-repeat;
  background-size: cover;
  height: 530px;
  margin-top: 180px;
}

.container {
  .txt {
    padding-top: 150px;
    font-size: 60px;
  }

  p {
    color: $gray;
    font-size: 20px;
  }

  button {
    padding: 15px 40px;
    margin: 20px;
    font-size: 14px;
    font-weight: bold;
    color: $dark;
    background-color: $lighter_aqua;

    span {
      margin: 0 20px;
    }

    &:hover {
      background-color: $pink;
      color: $light;
    }
  }
}
</style>