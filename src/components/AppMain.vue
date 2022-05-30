<template>
  <main>
      <section class="first-banner">

      </section>
  </main>
</template>

<script>
export default {

}
</script>

<style>
    .first-banner {
        height: 500px;
        background-image: url(../assets/theme_slider2_bg-1.jpg);
        background-position: center;
        background-size: cover;
        position: relative;
    }

    .first-banner::after {
        content: '';
        background-color: rgba(229, 103, 104, .9);
        position: absolute;
        top: 0;
        left: 0;
        width: 100%;
        height: 100%;
    }
</style>