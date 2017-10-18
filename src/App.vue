<template>
  <div id="app">
    <div class="container">
      <navbar />
      <router-view/>
      <home />
    </div>
  </div>
</template>

<script>
import Home from './components/Home'
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
    'navbar': Navbar,
    'home': Home
  }
}
</script>

<style lang="sass">
  @import '../node_modules/bulma/bulma.sass'
  @import './assets/style/mq'
  @import './assets/style/core'
</style>
