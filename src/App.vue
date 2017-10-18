<template>
  <div id="app">
    <div class="container">
      <navbar />
      <router-view/>
    </div>
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
  @import '../node_modules/bulma/bulma.sass'
  @import 'mq'
    
  .navbar
    padding: 2em
  .navbar-middle
    margin-left: 14em
  .nav-item
    margin-left: 4em
  .search-icon
    border-style: solid
    border-width: 2px
    border-color: #D8D8D8
    border-radius: 50%
    width: 42px
    height: 42px
    text-align: center
  .navbar-item img 
    max-height: 3em
  .img
    border-width: 1px
    border-radius: 50%
  .img-container
    width: 90px
    height: 50px
  .badge
    margin-left: -10px
    margin-top: -30px
  .badge-online
    margin-top: -20px
</style>
