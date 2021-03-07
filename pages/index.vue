<template>
  <div class="flame">
      <div class="top-text text-center"> -タロット占い-</div>
      <img class="d-block mx-auto mid-img" src="@/assets/original.png"/>
      <img class="d-block mx-auto mid-img" @click="showResult()" src="@/assets/move-tarot.gif"/>
      <div class="bottom-text text-center mt-5"> 願いを込めてカードをタップしてください。</div>
  </div>
</template>

<script>
export default {

methods: {
  showResult() {
    this.$router.push('/tarot-result/' + Math.floor(Math.random() * Math.floor(3)))
  }
}

}
</script>

<style>
.flame {
  background-color: #FFF6F5;
  width: 100vw;
  height: 100vh;
}

.top-text {
  font-family: 'M PLUS Rounded 1c', sans-serif;
  font-size: 150%;
  color: #444444;
  padding-top: 50px;

}

.bottom-text {
  font-family: 'M PLUS Rounded 1c', sans-serif;
  font-size: 100%;
  color: #444444;
}

.mid-img {
  margin-top: 50px;
  max-width: 500px;
  width: 80vw;
}
</style>
