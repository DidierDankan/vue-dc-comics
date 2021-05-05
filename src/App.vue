<template>
  <div id="app">
    <!-- Header -->
    <headerDC />

    <!-- Main -->
    <mainDC />

    <!-- Footer -->
    <footerDC />

  </div>
</template>

<script>
import headerDC from '@/components/headerDC.vue'
import mainDC from '@/components/mainDC.vue'
import footerDC from '@/components/footerDC.vue'

export default {
  name: 'App',
  components: {
    headerDC,
    mainDC,
    footerDC,

  }
}
</script>

<style lang="scss">
  /*  GENERALS */
  * {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  }

  body {
    font-family: sans-serif;
  }

  img {
    max-width: 100%;
  }

  /* UTILITIES */

  .container {
    max-width: 1000px;
    margin: 0 auto;
  }

  // .background-img-footer {
  //   background-image: url('@/assets/img/footer-bg.jpg');
  // }
</style>
