<template>
  <div class="text-center position-relative">
    <div class="txt">Working <strong class="fst-italic">process</strong></div>

    <div class="row justify-content-center m-0 p-0">
      <Working 
      class="col-2 m-0 p-0"
      v-for="(idea, index) in ideas" 
      :key="index"
      :imgI="idea.imgIdeas"
      :txtI="idea.textIdeas"
      :idI="idea.idIdeas"
      :colorI="idea.colorIdeas"
      />
    </div>

    <div class="position-absolute top-50">
      <img src="../assets/img/svg/wave.svg" alt="Wave">
    </div>
  </div>
</template>

<script>
import Working from "./Working.vue";

export default {
    name: "Process",
    components: {
      Working,

    },

    data(){
      return {
        ideas: [
          {
            imgIdeas: 'bi bi-lightbulb-fill',
            textIdeas: 'First theres an idea',
            idIdeas:'Lorem ipsum dolor sit, conetu adipisc sed be et ore aliqua pleasure itself.',
            colorIdeas: '#BADAC9' 
          },
          {
            imgIdeas: 'bi bi-chat',
            textIdeas: 'Then we talk about',
            idIdeas:'Lorem ipsum dolor sit, conetu adipisc sed be et ore aliqua pleasure itself.',
            colorIdeas: '#F8D12D'
          },
          {
            imgIdeas: 'bi bi-cloud-fill',
            textIdeas: 'And we think about',
            idIdeas:'Lorem ipsum dolor sit, conetu adipisc sed be et ore aliqua pleasure itself.',
            colorIdeas: '#80465F'
          },
          {
            imgIdeas: 'bi bi-pencil',
            textIdeas: 'So we draw along',
            idIdeas:'Lorem ipsum dolor sit, conetu adipisc sed be et ore aliqua pleasure itself.',
            colorIdeas: '#EB6950'
          },
        ]
      }
    }
}
</script>

<style scoped lang="scss">
@import "../style/general.scss";
@import "../style/general.scss";

.txt {
  font-size: 65px;
  margin-bottom: 100px;
  padding-top: 150px;
}

.position-absolute {
  left: 400px;
  z-index: -3;
}

</style>
