<template>
  <div class="ms_container ms_mt">
      <div class="row">
          <div class="col col-img">
              <img :src="require('../assets/Gavel-Illustration.png')" alt="">
          </div>
          <div class="col col-text">
              <h3>Law Faculty</h3>
              <p>Learing from world-leading academics and practioners, you'll not only receive an outstanding grounding in the theory of law, but you will be able to understand how those principles are applied in pratice through a range of student-led activities and competitions.</p>
              <button class="ms_btn-red">Read more</button>  
          </div>
      </div>
  </div>
</template>

<script>
export default {

}
</script>

<style lang="scss" scoped>
    .col-img > img {
        width: 15rem;
    }
</style>