<template>
  <div id="app">
    <AppHeader :menu="listMenu"/>
    <AppMain />
    <AppFooter />
  </div>
</template>

<script>
import AppHeader from './components/AppHeader.vue'
import AppMain from './components/AppMain.vue'
import AppFooter from './components/AppFooter.vue'

export default {
  name: 'App',
  components: {
    AppHeader,
    AppMain,
    AppFooter
  },
  data() {
    return {
      listMenu: [
        {
          text: "Home",
          active: true,
        },
        {
          text: "Courses",
          active: false,
        },
        {
          text: "About Us",
          active: false,
        },
        {
          text: "News",
          active: false,
        },
        {
          text: "Pages",
          active: false,
        },
        {
          text: "Collectibles",
          active: false,
        },
        {
          text: "Contact",
          active: false,
        },
        {
          text: "Purchase",
          active: false,
        },
      ],
    }
  }
}
</script>

<style lang="scss">
@import "./style/common.scss";
</style>
