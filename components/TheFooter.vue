<template>
  <footer id="footer" class="footer-area">
    <div class="container">
      <div class="footer-copyright">
        <div class="row">
          <div class="col-lg-12">
            <div class="copyright copyright-content d-sm-flex justify-content-between">
              <p class="text" style=" width: 100%; text-align: center">
                2022 — <a href="https://shawee.io/pt/"><strong>FF HACKATHON</strong></a>
              </p>
            </div> <!-- copyright -->
          </div>
        </div> <!-- row -->
      </div> <!-- footer copyright -->
    </div> <!-- container -->
    <Particles
      id="particles-2"
      class="particles"
      url="particles.json"
    />
  </footer>
</template>

<script>
import Particles from 'particles.vue'
import Vue from 'vue'
Vue.use(Particles)

export default {}
</script>

<style scoped>
.bg_cover {
  background: url('~assets/basic/assets/images/footer-bg.svg');
}
</style>
