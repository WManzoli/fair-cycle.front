<template>
  <div style="background: #fff;">
    <TheNavbar />
    <ThePanel />
  </div>
</template>

<script>
export default {
  data () {
    return {
      teste: ''
    }
  },
  mounted () {
    this.$router.push('/home')
  }
}
</script>

  <style>
  </style>
