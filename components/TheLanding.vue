<template>
  <header class="header-area" style="background: #000">
    <div id="home" class="header-hero bg_cover">
      <div class="container">
        <div class="row justify-content-center">
          <div class="w-100">
            <div class="header-hero-content">
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
          <div class="w-100">
            <div class="header-hero-image text-center wow fadeIn" data-wow-duration="1.3s" data-wow-delay="1.4s">
              <!--              <img src="~/assets/basic/assets/images/header-hero.png" alt="hero">-->
            </div> <!-- header hero image -->
          </div>
        </div> <!-- row -->
        <div class="d-flex pb-50 mx-auto " style="gap: 1rem;">
          <v-card
            class="carousel"
            elevation="24"
            max-width="33%"
          >
            <v-list two-line>
              <v-list-item>
                <v-list-item-avatar class="bg-success">
                  <v-icon>mdi-parking</v-icon>
                </v-list-item-avatar>
                <v-list-item-content class="pl-2">
                  <v-list-item-title>Estacionamentos</v-list-item-title>
                  <v-list-item-subtitle>Bike Friendly & 24/7</v-list-item-subtitle>
                </v-list-item-content>
              </v-list-item>
            </v-list>

            <v-carousel
              :show-arrows="false"
              height="250px"
            >
              <v-carousel-item
                v-for="(item,i) in items1"
                :key="i"
                eager
              >
                <v-img :src="item.src" height="100%" eager />
              </v-carousel-item>
            </v-carousel>
            <v-system-bar lights-out />
          </v-card>
          <v-card
            class="carousel"
            elevation="24"
            max-width="33%"
          >
            <v-list two-line>
              <v-list-item>
                <v-list-item-avatar class="bg-warning">
                  <v-icon>mdi-bicycle</v-icon>
                </v-list-item-avatar>
                <v-list-item-content class="pl-2">
                  <v-list-item-title>Bicicletarias</v-list-item-title>
                  <v-list-item-subtitle>Reparos e Trocas</v-list-item-subtitle>
                </v-list-item-content>
              </v-list-item>
            </v-list>

            <v-carousel
              :show-arrows="false"
              height="250px"
            >
              <v-carousel-item
                v-for="(item,i) in items2"
                :key="i"
                eager
              >
                <v-img :src="item.src" height="100%" eager />
              </v-carousel-item>
            </v-carousel>
            <v-system-bar lights-out />
          </v-card>
          <v-card
            class="carousel"
            elevation="24"
            max-width="33%"
          >
            <v-list two-line>
              <v-list-item>
                <v-list-item-avatar class="bg-info">
                  <v-icon>mdi-handcuffs</v-icon>
                </v-list-item-avatar>
                <v-list-item-content class="pl-2">
                  <v-list-item-title>Segurança</v-list-item-title>
                  <v-list-item-subtitle>Segurar bens e comercios</v-list-item-subtitle>
                </v-list-item-content>
              </v-list-item>
            </v-list>

            <v-carousel
              :show-arrows="false"
              height="250px"
            >
              <v-carousel-item
                v-for="(item,i) in items3"
                :key="i"
                eager
              >
                <v-img :src="item.src" height="100%" eager />
              </v-carousel-item>
            </v-carousel>
            <v-system-bar lights-out />
          </v-card>
        </div>
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
      colors: [
        'green',
        'secondary',
        'yellow darken-4',
        'red lighten-2',
        'orange darken-1'
      ],
      items1: [
        {
          src: 'https://images.unsplash.com/photo-1587485715817-5e8c6fa2a903?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1587&q=80'
        },
        {
          src: 'https://images.unsplash.com/photo-1554135386-1a06027310a5?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1587&q=80'
        }
      ],
      items2: [
        {
          src: 'https://images.unsplash.com/photo-1607109181641-74f8e7f4eb11?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1587&q=80'
        },
        {
          src: 'https://images.unsplash.com/photo-1601067095185-b8b73ad7db10?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1526&q=80'
        }
      ],
      items3: [
        {
          src: 'https://images.unsplash.com/photo-1450101499163-c8848c66ca85?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=870&q=80'
        },
        {
          src: 'https://images.unsplash.com/photo-1637763723578-79a4ca9225f7?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=871&q=80'
        }
      ],
      cycle: true,
      slides: [
        'https://cdn.vuetifyjs.com/images/john.png',
        'https://cdn.vuetifyjs.com/images/john.png',
        'https://cdn.vuetifyjs.com/images/john.png',
        'https://cdn.vuetifyjs.com/images/john.png',
        'https://cdn.vuetifyjs.com/images/john.png'
      ]
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
