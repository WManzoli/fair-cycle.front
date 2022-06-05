<template>
  <header class="header-area" style="background: #000">
    <div id="home" class="header-hero bg_cover">
      <div class="container" style="min-height: 100vh;">
        <div class="row">
          <div class="col-lg-12">
            <div class="header-hero-image text-center wow fadeIn" data-wow-duration="1.3s" data-wow-delay="1.4s">
              <!--              <img src="~/assets/basic/assets/images/header-hero.png" alt="hero">-->
            </div> <!-- header hero image -->
          </div>
        </div> <!-- row -->
      </div> <!-- container -->
    </div> <!-- header hero -->
  </header>
</template>

<script>

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

</style>
