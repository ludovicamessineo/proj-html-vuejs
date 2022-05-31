<template>
  <div class="courses ms_container ms_mt">
      <div class="row">
          <div class="col col-text">
              <img :src="require('../assets/Books-icon.png')" alt="">
              <h2>Thousands of courses for any type of student</h2>
              <p>At EduPrime, it doesn't matter what domain you wish to pursue a career in. Here you can find a course that satisfies your needs within a click away and applies for a course in a matter of minutes. EduPrime is ranked as the most versatile university in the world, thanks to the number of courses it provides.</p>
              <button class="ms_btn">Browse through courses</button>
          </div>
          <div class="col col-img">
              <img :src="require('../assets/Graduation-Illustration.png')" alt="">
          </div>
      </div>
  </div>
</template>

<script>
export default {

}
</script>

<style>
.col-text > img {
    width: 3rem;
    margin-bottom: 1rem;
}

.col-img > img {
    padding: 3rem 0;
}
</style>