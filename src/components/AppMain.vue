<template>
  <main>
      <section class="first-banner">
          <div class="ms_container">
             <h2>Key for your success</h2>
             <p>EduPrime is the most versatile WordPress theme for educational purposes, showcasing universities, courses, secondary schools etc.</p>
          </div>
      </section>

      <section >
          <AppSectionText />
      </section>

      <section class="course-option">
          <div class="ms_container ms_mt text-center">
            <h2>Faculties available at EduPrime</h2>
            <p>A single university with a load of courses, tailored <br> to satisfy any student's needs. </p>
            <ul class="course-card d-flex">
                <li v-for="(item, index) in imgCard" :key="index" class="d-flex flex-column">
                    <img :src="require(`../assets/${item.img}`)" alt="">
                    <small> {{item.text}} </small>
                </li>
            </ul>
            
          </div>
      </section>
  </main>
</template>

<script>
import AppSectionText from './AppSectionText.vue'

export default {
    name: 'AppMain',
    components: {
        AppSectionText
    },
    data() {
       return {
           imgCard: [
               {
                   img: "Gavel-v2.png",
                   text: "Law Faculty",
                   active: true
               },
               {
                   img: "Coins-tabs-v2.png",
                   text: "Economy",
                   active: false
               },
               {
                   img: "Medicine-tabs-v2.png",
                   text: "Medicine",
                   active: false
               },
               {
                   img: "Computer-tabs-v2.png",
                   text: "Computer Science",
                   active: false
               },
               {
                   img: "Palette-tabs-v2.png",
                   text: "Graphic",
                   active: false
               }
           ]
       } 
    }
}
</script>

<style>
    .first-banner {
        height: 500px;
        background-image: url(../assets/theme_slider2_bg-1.jpg);
        background-position: center;
        background-size: cover;
        position: relative;
        color: white;
        display: flex;
        justify-content: center;
        align-items: center;
        text-align: center;
    }

    .first-banner::before {
        content: '';
        background-color: rgba(229, 103, 104, .9);
        position: absolute;
        top: 0;
        left: 0;
        width: 100%;
        height: 100%;
    }

    .course-card img {
        width: 5rem;
    }
</style>