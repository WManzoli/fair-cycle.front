<template>
  <header class="header-area" style="background: #000">
    <div id="home" class="header-hero bg_cover">
      <div class="container">
        <div class="row justify-content-center">
          <div class="col-lg-12">
            <div class="header-hero-content pb-200">
              <section class="wrapper">
                <h2 class="header-sub-title wow fadeInUp" data-wow-duration="1.3s" data-wow-delay="0.2s">
                  <div class="rw-words rw-words-2">
                    <div>
                      Precisando de
                      <span>&nbsp;</span>
                      <span>garagem?</span>
                      <span>manutenção?</span>
                      <span>segurança?</span>
                      <span>seguros?</span>
                      <span>atendimento?</span>&nbsp;
                    </div>
                  </div>
                </h2>
              </section>
              <h2 class="header-title wow fadeInUp" data-wow-duration="1.3s" data-wow-delay="0.5s">
                A Fair Cycle pode te ajudar !
              </h2>
              <p class="text wow fadeInUp" data-wow-duration="1.3s" data-wow-delay="0.8s">
                Bike friendly spots for your issues pot.
              </p>
              <p class="main-btn wow fadeInUp" data-wow-duration="1.3s" data-wow-delay="1.1s" @click="handleClick()">
                Saber mais...
              </p>
            </div> <!-- header hero content -->
          </div>
        </div> <!-- row -->
        <div class="row">
          <div class="col-lg-12">
            <div class="header-hero-image text-center wow fadeIn" data-wow-duration="1.3s" data-wow-delay="1.4s">
              <!--              <img src="~/assets/basic/assets/images/header-hero.png" alt="hero">-->
            </div> <!-- header hero image -->
          </div>
        </div> <!-- row -->
      </div> <!-- container -->
      <Particles
        id="particles-1"
        class="particles"
        style="pointer-events: none !important;"
        url="particles.json"
      />
    </div> <!-- header hero -->
  </header>
</template>

<script>
import Particles from 'particles.vue'
import Vue from 'vue'
Vue.use(Particles)

export default {
  data () {
    return {
      // currentWord: '',
      // currentWordArray: ['Segurança', 'Atendimento', 'Manutenção', 'Garagem']
    }
  },
  methods: {
    handleClick () {
      window.setTimeout(function () { window.blipClient.toogleChat() })
    }
  }
}
</script>

<style scoped>
.bg_cover {
  background-image: url('~assets/basic/assets/images/banner-bg.svg');
}
.wrapper{
  display: flex;
  width: 100%;
  font-size : 4vh;
}
.rw-words span{
  position: absolute;
  opacity: 0;
  overflow: hidden;
  width: 100%;
  /* color: black; */
  /* background-color:black; */
}
.rw-sentence span{
  color: #444;
  white-space: nowrap;
  font-size: 200%;
  font-weight: normal;
}
.rw-words-2 span{
  animation: rotateWordsSecond 10s linear infinite 0s;
}
.rw-words span:nth-child(2) {
  animation-delay: 2s;
  color: #fff;
}
.rw-words span:nth-child(3) {
  animation-delay: 4s;
  color: #fff;
}
.rw-words span:nth-child(4) {
  animation-delay: 6s;
  color: #fff;
}
.rw-words span:nth-child(5) {
  animation-delay: 8s;
  color: #fff;
}
.rw-words span:nth-child(6) {
  animation-delay: 10s;
  color: #fff;
}
@keyframes rotateWordsSecond {
  0% { opacity: 2; animation-timing-function: ease-out; width: 0px; }
  10% { opacity: 1; width: 20%; }
  20% { opacity: 1; width: 30%; }
  27% { opacity: 0; width: 50%; }
  /* 100% { opacity: 0; } */
}
</style>
