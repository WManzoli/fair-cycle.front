<template>
  <div style="background: #000;">
    <TheNavbar />
    <TheLanding />
    <TheFooter />
    <!--    <BackToTopButton />-->
  </div>
</template>

<script>
import { BlipChat } from 'blip-chat-widget'
import TheNavbar from '@/components/TheNavbar'
import TheLanding from '@/components/TheLanding'
import TheFooter from '@/components/TheFooter'
// import BackToTopButton from '@/components/BackToTopButton'
import '../../node_modules/animate.css/animate.css'

window.blipClient = new BlipChat()
  .withAppKey('ZmFpcmN5Y2xlOmNiNzkyYjMzLTJlMzMtNDhkZi04NDRiLWI0YWZmMTAzODJhOQ==')
  .withButton({ height: '200px', color: '#fff', icon: 'https://blipmediastore.blob.core.windows.net/public-medias/Media_3c9fe1e9-a50d-4f51-bc4e-a5e6122711e0' })
  .withTarget('page-wrap')
  .withCustomCommonUrl('https://chat.blip.ai/')
window.blipClient.build()

// Bootstrap CSS
require('assets/basic/assets/css/bootstrap.min.css')
// Default CSS
require('assets/basic/assets/css/default.css')
// Style CSS
require('assets/basic/assets/css/style.css')

export default {
  components: {
    TheNavbar,
    TheLanding,
    TheFooter
    // BackToTopButton

  },
  head () {
    return {
      title: 'Home',
      meta: [
        // hid is used as unique identifier. Do not use `vmid` for it as it will not work
        {
          hid: 'Landing page'
          // name: 'description',
          // content: 'My custom description'
        }
      ]
    }
  }
}
</script>

<style>
html {
  scroll-behavior: smooth;
}
</style>
