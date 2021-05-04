<template>
  <footer >
      <div class="bg-img">
          <img src="@/assets/img/footer-bg.jpg" alt="footer bg">
        <div class="container">
            whats up
        </div>
      </div>
  </footer>
</template>

<script>
export default {
    name:'footerDC',
}
</script>

<style scoped>
    footer {
        position: relative;
    }
    .bg-img {
        width: 100%;
        position: absolute;
        z-index: -1;
    }

    .bg-img img {
        width: 100%;
    }

</style>