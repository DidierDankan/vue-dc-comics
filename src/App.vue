<template>
  <div id="app">
    <!-- Header -->
    <headerDC />

    <!-- Main -->


    <!-- Footer -->

  </div>
</template>

<script>
import headerDC from '@/components/headerDC.vue'

export default {
  name: 'App',
  components: {
    headerDC
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

  /* UTILITIES */

  .container {
    max-width: 1000px;
    margin: 0 auto;
  }
</style>
