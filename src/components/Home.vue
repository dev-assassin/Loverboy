<template>
<div>
  <section class="hero is-light">
    <div class="container">
      <div class="hero-body">
        <h1 class="title Graphik-Bold-Web hero-title">Loverboy er Danmarks største og mest besøgte online community for homo, bi og transseksuelle.</h1>
        <button class="button is-dark is-large hero-button Graphik-Bold-Web" @click="showModal = true"><i class="fa fa-user user-icon " />&nbsp;Join today</button>
        <div class="modal is-active" v-if="showModal">
          <div class="modal-background"></div>
          <div class="modal-content box">
            <div class="tabs is-centered is-medium">
              <ul class="register Graphik-Bold-Web">
                <li class="is-active"><a>Join</a></li>
                <li><a style="color:#eee">Log in</a></li>
              </ul>
            </div>
            <div class="field">
              <div class="control">
                <input class="input is-large" type="text" placeholder="Name">
                <input class="input is-large" type="email" placeholder="Email">
                <input class="input is-large" type="password" placeholder="Password">
                <button class="button is-dark is-large" style="width:100%"><i class="fa fa-user user-icon " />&nbsp;Join</button>
                <h1 class="signup">Sign up with</h1>
                <div class="level">
                  <button class="button is-info is-large level-item">Facebook</button>
                  <button class="button is-danger is-large level-item">Google</button>
                </div>
                <p style="text-align:center">Some legal desclamer to get rid of mandatory<p>
                <p style="text-align:center; margin-bottom:30px">check boxes and validation</p>
              </div>
            </div>
          </div>
          <button class="modal-close is-large" aria-label="close" @click="showModal = false"></button>
        </div>
      </div>
    </div>
  </section>
  <div class="container">
    <nav class="level">
      <div class="level-left">
        <section class="section">
            <h2 class="title Graphik-Bold-Web">Newest users</h2>
            <h2 class="subtitle Graphik-Regular-Web">8 users have joined today</h2>
        </section>
      </div>
      <div class="level-right">
        <a class="button is-outlined is-medium"><i class="fa fa-user-plus" style="margin-right: 10px"></i> View new users</a>
      </div>
    </nav>
    <div class="columns">
      <div class="column is-3">
        <div class="box">
          <img src="../assets/images/default user.jpeg" alt="user icon" width="68" height="80">
          <div class="user-card">
            <p class="Graphik-Bold-Web card-name">Shawn Peterson</p>
            <p class="Graphik-Regular-Web card-content">Danielton</p>
            <p class="Graphik-Regular-Web card-content">Venner</p>
          </div>
        </div>
      </div>
      <div class="column is-3">
        <div class="box">
          <img src="../assets/images/default user.jpeg" alt="user icon" width="68" height="80">
          <div class="user-card">
            <p class="Graphik-Bold-Web card-name">Shawn Peterson</p>
            <p class="Graphik-Regular-Web card-content">Danielton</p>
            <p class="Graphik-Regular-Web card-content">Venner</p>
          </div>
        </div>
      </div>
      <div class="column is-3">
        <div class="box">
          <img src="../assets/images/default user.jpeg" alt="user icon" width="68" height="80">
          <div class="user-card">
            <p class="Graphik-Bold-Web card-name">Shawn Peterson</p>
            <p class="Graphik-Regular-Web card-content">Danielton</p>
            <p class="Graphik-Regular-Web card-content">Venner</p>
          </div>
        </div>
      </div>
      <div class="column is-3">
        <div class="box">
          <img src="../assets/images/default user.jpeg" alt="user icon" width="68" height="80">
          <div class="user-card">
            <p class="Graphik-Bold-Web card-name">Shawn Peterson</p>
            <p class="Graphik-Regular-Web card-content">Danielton</p>
            <p class="Graphik-Regular-Web card-content">Venner</p>
          </div>
        </div>
      </div>
    </div>
    <nav class="level">
      <div class="level-left">
        <section class="section">
            <h2 class="title Graphik-Bold-Web">Currently online</h2>
            <h2 class="subtitle Graphik-Regular-Web">There are 2345 online users now</h2>
        </section>
      </div>
      <div class="level-right">
        <a class="button is-outlined is-medium"><span class="badge is-badge-small" data-badge=""><i class="fa fa-users"></i></span><span style="margin-left: 15px">View all online users</span></a>
      </div>
    </nav>
    <div class="columns">
      <div class="column is-3">
        <div class="box">
          <img src="../assets/images/default user.jpeg" alt="user icon" width="68" height="80">
          <div class="user-card">
            <p class="Graphik-Bold-Web card-name">Shawn Peterson</p>
            <p class="Graphik-Regular-Web card-content">Danielton</p>
            <p class="Graphik-Regular-Web card-content">Venner</p>
          </div>
        </div>
      </div>
      <div class="column is-3">
        <div class="box">
          <img src="../assets/images/default user.jpeg" alt="user icon" width="68" height="80">
          <div class="user-card">
            <p class="Graphik-Bold-Web card-name">Shawn Peterson</p>
            <p class="Graphik-Regular-Web card-content">Danielton</p>
            <p class="Graphik-Regular-Web card-content">Venner</p>
          </div>
        </div>
      </div>
      <div class="column is-3">
        <div class="box">
          <img src="../assets/images/default user.jpeg" alt="user icon" width="68" height="80">
          <div class="user-card">
            <p class="Graphik-Bold-Web card-name">Shawn Peterson</p>
            <p class="Graphik-Regular-Web card-content">Danielton</p>
            <p class="Graphik-Regular-Web card-content">Venner</p>
          </div>
        </div>
      </div>
      <div class="column is-3">
        <div class="box">
          <img src="../assets/images/default user.jpeg" alt="user icon" width="68" height="80">
          <div class="user-card">
            <p class="Graphik-Bold-Web card-name">Shawn Peterson</p>
            <p class="Graphik-Regular-Web card-content">Danielton</p>
            <p class="Graphik-Regular-Web card-content">Venner</p>
          </div>
        </div>
      </div>
    </div>
  </div>
</div>
</template>

<script>
export default {
  name: 'Home',
  data () {
    return {
      showModal: false
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="sass" scoped>
</style>
