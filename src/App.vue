<template>
  <div id="app">
    <navbar />
    <router-view/>
  </div>
</template>

<script>
import Navbar from './components/Navbar'
export default {
  name: 'app',
  data: function () {
    return {
    }
  },
  methods: {
  },
  components: {
    'navbar': Navbar
  }
}
</script>

<style lang="sass">
  $box-padding: 0em
  $box-shadow: 4px 2px 8px 0 rgba(0,0,0,0.06), 0 2px 4px 0 rgba(0,0,0,0.09)
  @import '../node_modules/bulma/bulma.sass'
  @import './assets/style/mq'
  @import './assets/style/core'
  @import '../node_modules/bulma-badge/badge.sass'
</style>
