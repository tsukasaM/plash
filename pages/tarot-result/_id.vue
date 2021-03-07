<template>
  <div class="result-flame">
      <img class="d-block mx-auto head_frame pt-5" src="@/assets/head_frame.png"/>
      <img class="d-block mx-auto card-img mt-5 " :src = this.imgSrc />  
        <tarot-result-context :id= this.$route.params.id></tarot-result-context>
      <img class="d-block mx-auto head_frame" src="@/assets/bottom_frame.png"/>
      <br>
      <div style="text-align: center;">
        <nuxt-link to="/" style="color: #db7093;">戻る</nuxt-link>
      </div>
      <br>
  </div>
</template>

<script>
import tarot_result_context from '../../components/tarot-result-context.vue'

export default {
  components: { tarot_result_context },

  data() {
    return {
      imgSrc: require("@/assets/tarot_result/result_" + this.$route.params.id + ".png"),
    }
  }
}
</script>

<style>
.result-flame {
  background-color: #ffffff;
  width: 100vw;
  height: 100vh;
}

.mid-text {
  font-family: 'M PLUS Rounded 1c', sans-serif;
  font-size: 150%;
  color: #444444;
}

.head_frame {
  max-width: 300px;
  width: 80vw;
}

.card-img {
  max-width: 300px;
  width: 60vw;
}

.result-context {
 text-align: center;
  font-family: 'M PLUS Rounded 1c', sans-serif;
  font-size: 100%;
  line-height: 100%;
  color: #444444;
}


</style>
