<template lang="pug">
  #app
    img(src="./assets/logo.png")
    router-view
    navigation
</template>

<script>
import Navigation from '@/components/Navigation'
export default {
  name: 'app',
  data () {
    return {
      css: ''
    }
  },
  components: {
    Navigation
  }
}
</script>

<style lang="sass">
@import '/assets/style/config'
@import '/assets/style/mixins'
#app
  font-family: 'Avenir', Helvetica, Arial, sans-serif
  -webkit-font-smoothing: antialiased
  -moz-osx-font-smoothing: grayscale
  text-align: center
  color: #2c3e50
  margin-top: 60px

</style>
