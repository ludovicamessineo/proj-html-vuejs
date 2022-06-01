<template>
  <main>
      <!-- BANNER -->
      <section class="first-banner">
          <div class="ms_container">
             <h2>Key for your success</h2>
             <p>EduPrime is the most versatile WordPress theme for educational purposes, showcasing universities, courses, secondary schools etc.</p>
          </div>
      </section>
      <!-- /BANNER -->


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

      <section> 
          <AppSectionImg />
      </section>

      <section class="events ms_mt">
          <div class="ms_container">
              <div class="uni-graphic">
                  <img class="icon" :src="require('../assets/Clock-and-Bell.png')" alt="">  
                  <h2>University Year</h2>  
                  <div class="timeline">
                      <div class="timeline-img">
                        <img :src="require('../assets/Timeline-Item.png')" alt="">                     
                      </div>
                      <div class="timeline-text">
                          
                      </div>
                  </div>
              </div>

              <div class="uni-events">
                  <img class="icon" :src="require('../assets/upcoming-events-calendar-icon.png')" alt="">
                  <h2>Upcoming Events</h2>
                  <div class="row">
                      <div class="col card" v-for="(item, index) in coachingCard" :key="index">
                          <h4> {{item.title}} </h4>
                          <small> {{item.date}} </small>
                          <p> {{item.text}} </p>
                          <button class="ms_btn-red">Find More</button>
                      </div>
                  </div>
                  <button class="ms_btn mt-4">View all Events</button>
              </div>
          </div>
      </section>

      <section>
          <div class="ms_container ms_mt">
              <h3>Latest courses</h3>
              <div class="row">
                  <div class="col course-card" v-for="(item, index) in courseCard" :key="index">
                      <img :src="require(`../assets/${item.img}`)" alt="">
                      <h5> {{item.text}} </h5>
                      <p> {{item.teacher}} </p>
                      <p> {{item.price}} </p>
                  </div>
              </div>

              <div class="row m-3">
                  <div class="col">
                      <img class="icon" :src="require('../assets/Exam-icon.png')" alt="">
                      <h3>The most efficient examination method</h3>
                      <p>EduPrime has gathered teachers from around the globe to brainstorm in order to facilitate the evaluation of our students. Every teacher from our university has an influence on how students are evaluated at his/her subject.</p>
                      <button class="ms_btn-red">Discover the Method</button>
                  </div>
                  <div class="col">
                      <img :src="require('../assets/Exam-Illustration.png')" alt="">
                  </div>
              </div>

              <div class="row m-5">
                  <div class="col">
                      <img :src="require('../assets/Girl-Illustration.png')" alt="">
                  </div>
                  <div class="col">
                      <img class="icon" :src="require('../assets/Exam-icon.png')" alt="">
                      <h3>Variable fees for international students</h3>
                      <p>EduPrime has gathered teachers from around the globe to brainstorm in order to facilitate the evaluation of our students. Every teacher from our university has an influence on how students are evaluated at his/her subject.</p>
                      <button class="ms_btn-red">List of Fees</button>
                  </div>
              </div>
          </div>
      </section>

      <AppCta />


  </main>
</template>

<script>
import AppSectionText from './AppSectionText.vue'
import AppSectionImg from './AppSectionImg.vue'
import AppCta from './AppCta.vue'

export default {
    name: 'AppMain',
    components: {
        AppSectionText,
        AppSectionImg,
        AppCta
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
           ],
            coachingCard: [
                {
                    title: "Coaching Session",
                    date: "20 May 21.30 PM",
                    text: "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor[...]"                   
                },
                {
                    title: "Coaching Session",
                    date: "24 Mar 18.00 PM",
                    text: "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor[...]"  
                }, 
                {
                    title: "Coaching Session",
                    date: "12 Feb 13.30 PM",
                    text: "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor[...]"  
                }
            ],
            courseCard: [
                {
                    img: "Decisions-icon.png",
                    text: "Make Better Decisions",
                    teacher: "Teacher: James Collins",
                    price: "Price: $21.00"
                },
                {
                    img: "Speaker-icon.png",
                    text: "How to be a speaker",
                    teacher: "Teacher: James Collins",
                    price: "Price: Free"
                },
                {
                    img: "Network-icon.png",
                    text: "Network Introductions",
                    teacher: "Teacher: James Collins",
                    price: "Price: Free"
                },
                {
                    img: "Brand-icon.png",
                    text: "Brand Management",
                    teacher: "Teacher: James Collins",
                    price: "Price: Free"
                }
            ]
        }
    }
}
</script>

<style lang="scss" scoped>
    /* SECTION 1 */
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
    /* /SECTION 1 */

    /* SECTION 3 */
    .course-card > li {
        padding: 1.4rem 2rem;
        font-size: .8rem;
        border: 1px solid lightgrey;
        color: #e56768;
    }

    .course-card img {
        width: 5rem;
        padding-bottom: .5rem;
    }
    /* /SECTION 3 */

    // SECTION 5
    .events {
        background-color: #e56768;
        text-align: center;
        color: white;
    }

    .card {
        background-color: white;
        color: black;
        margin: 2rem .5rem;
        padding: .8rem .4rem;
        border-radius: 10px;
        font-size: .7rem;
        position: relative;

        button {
            padding: .4rem .6rem;
            width: 5rem;
            position: absolute;
            left: 35%;
            bottom: -15px;
            box-shadow: 1px 1px 5px black;
        }
    }
    // SECTION 5

    // SECTION 6
    .course-card {
       border: 1px solid lightgray; 
       text-align: center;
       font-size: .6rem;
       margin: 1rem;
       padding: .8rem;

       img {
           width: 3rem;
       }
    }
</style>