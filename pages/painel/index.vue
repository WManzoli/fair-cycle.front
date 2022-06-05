<template>
  <div style="background: #fff;">
    <TheNavbar />
    <ThePanel />
  </div>
</template>

<script>
import { BlipChat } from 'blip-chat-widget'
import TheNavbar from '@/components/TheNavbar'
import ThePanel from '@/components/ThePanel'
import '../../node_modules/animate.css/animate.css'

window.blipClient = new BlipChat()
  .withAppKey('ZmFpcmN5Y2xlOmNiNzkyYjMzLTJlMzMtNDhkZi04NDRiLWI0YWZmMTAzODJhOQ==')
  .withButton({ color: '#134f5cff', icon: 'https://blipmediastore.blob.core.windows.net/public-medias/Media_facbbeb5-1e48-479e-b117-9c59138c6071' })
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
    ThePanel
  },
  head () {
    return {
      title: 'Painel',
      meta: [
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
