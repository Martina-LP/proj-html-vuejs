<template>
  <div class="mt-3 ideas">
    <i :class="imgI" class="font-i"></i>
      <div class="p-3">
        <div class="h5"> {{txtI}} </div>
        <span> {{idI}} </span>
      </div>
  </div>
</template>

<script>
export default {
  name: "Working",
  props: {
    imgI: String,
    txtI: String,
    idI: String,
    colorI: String

  }
}
</script>

<style scoped lang="scss">
.font-i {
  font-size: 50px;
  padding:55px 60px;
  border-radius: 50%;
  background-color: #faf7f1;
  color: #badac9;
}

.h5 {
  margin-top: 55px;
}

span {
  line-height: 1.8;
  color:#828282;
}

</style>
