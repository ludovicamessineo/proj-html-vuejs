<template>
  <div class="header d-flex justify-content-between align-items-center">
    <div class="header-logo">
        <img :src="require('../assets/theme_eduprime_logo.png')" alt="">
    </div>
    <div class="header-menu d-flex">
        <ul class="d-flex align-items-center">
            <li
            v-for="(item, index) in menu" 
            :key="index"
            ><a href=""> {{item.text}} </a></li>
        </ul>
        <button class="ms_btn text-uppercase">View Courses</button>
    </div>
  </div>
</template>

<script>
export default {
    name: 'AppHeader',
    props: {
        menu: Array
    }
}
</script>

<style lang="scss" scoped>
.header {
    width: 100%;
    height: 80px;
    padding: 2rem;
    background-color: rgba(229, 103, 104, .1);
    position: fixed;
    left: 0;
    top: 0;
    z-index: 10;

    img {
        width: 10rem;
    }

    ul {
        margin: 0;

        li {
            padding: .4rem;
            font-size: .8rem;
            font-weight: 800;
            color: white;
        }
    }
}
</style>