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
  <div class="container" style="padding: 2em">
    <nav class="level">
      <div class="level-left">
        <section class="section">
            <h2 class="title Graphik-Bold-Web">Newest users</h2>
            <h2 class="subtitle Graphik-Regular-Web">8 users have joined today</h2>
        </section>
      </div>
      <div class="level-right">
        <a class="button is-outlined is-medium button-radius"><i class="fa fa-user-plus" style="margin-right: 10px"></i> View new users</a>
      </div>
    </nav>
    <div class="columns" v-for="rowIndex in this.newUsers.length" :key="rowIndex">
      <div class="column is-3" v-for="(user, index) in newUsers.slice(4*(rowIndex-1), 4*(rowIndex-1)+4)" :key="index">
        <div class="box">
          <div class="level">
            <div class="level-left">
              <img src="../assets/images/images.jpeg" class="img-user" alt="user icon" width="68" height="80">
            </div>
            <div class="level-item">
              <div class="user-card">
                <p class="Graphik-Bold-Web card-name">{{user.name}}</p>
                <p class="Graphik-Regular-Web card-content">{{user.city.name}}</p>
                <p class="Graphik-Regular-Web card-content">{{user.target.name}} * 42</p>
              </div>
            </div>
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
        <a class="button is-outlined is-medium button-radius"><span class="badge is-badge-small" data-badge=""><i class="fa fa-users"></i></span><span style="margin-left: 15px">View all online users</span></a>
      </div>
    </nav>
    <div class="columns" v-for="rowIndex in this.onlineUsers.length" :key="rowIndex">
      <div class="column is-3" v-for="(user, index) in onlineUsers.slice(4*(rowIndex-1), 4*(rowIndex-1)+4)" :key="index">
        <div class="box">
          <div class="level">
            <div class="level-left">
              <img src="../assets/images/images.jpeg" class="img-user" alt="user icon" width="68" height="80">
            </div>
            <div class="level-item">
              <div class="user-card">
                <p class="Graphik-Bold-Web card-name">{{user.name}}</p>
                <p class="Graphik-Regular-Web card-content">{{user.city.name}}</p>
                <p class="Graphik-Regular-Web card-content">{{user.target.name}} * 42</p>
              </div>
            </div>
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
      users: [
        {
          'id': 101,
          'email': 'user_0@example.com',
          'city_id': 50,
          'target_id': 2,
          'birthdate': '1976-02-08',
          'about': 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.',
          'name': 'User 0',
          'created_at': '2017-10-17T18:06:10.805Z',
          'updated_at': '2017-10-17T18:06:10.805Z',
          'url': 'http://localhost:3000/users/101.json',
          'city': {
            'id': 50,
            'name': 'Randers'
          },
          'target': {
            'id': 2,
            'name': 'Dates'
          }
        },
        {
          'id': 102,
          'email': 'user_1@example.com',
          'city_id': 20,
          'target_id': 3,
          'birthdate': '1986-04-07',
          'about': 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.',
          'name': 'User 1',
          'created_at': '2017-10-17T18:06:10.947Z',
          'updated_at': '2017-10-17T18:06:10.947Z',
          'url': 'http://localhost:3000/users/102.json',
          'city': {
            'id': 20,
            'name': 'Aabenraa'
          },
          'target': {
            'id': 3,
            'name': 'Just looking'
          }
        },
        {
          'id': 103,
          'email': 'user_2@example.com',
          'city_id': 42,
          'target_id': 2,
          'birthdate': '1967-06-21',
          'about': 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.',
          'name': 'User 2',
          'created_at': '2017-10-17T18:06:11.080Z',
          'updated_at': '2017-10-17T18:06:11.080Z',
          'url': 'http://localhost:3000/users/103.json',
          'city': {
            'id': 42,
            'name': 'Otterup'
          },
          'target': {
            'id': 2,
            'name': 'Dates'
          }
        },
        {
          'id': 104,
          'email': 'user_3@example.com',
          'city_id': 106,
          'target_id': 4,
          'birthdate': '1960-05-05',
          'about': 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.',
          'name': 'User 3',
          'created_at': '2017-10-17T18:06:11.215Z',
          'updated_at': '2017-10-17T18:06:11.215Z',
          'url': 'http://localhost:3000/users/104.json',
          'city': {
            'id': 106,
            'name': 'Hvidovre'
          },
          'target': {
            'id': 4,
            'name': 'Nothing'
          }
        },
        {
          'id': 105,
          'email': 'user_4@example.com',
          'city_id': 12,
          'target_id': 2,
          'birthdate': '1975-02-14',
          'about': 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.',
          'name': 'User 4',
          'created_at': '2017-10-17T18:06:11.348Z',
          'updated_at': '2017-10-17T18:06:11.348Z',
          'url': 'http://localhost:3000/users/105.json',
          'city': {
            'id': 12,
            'name': 'Vig'
          },
          'target': {
            'id': 2,
            'name': 'Dates'
          }
        },
        {
          'id': 106,
          'email': 'user_5@example.com',
          'city_id': 118,
          'target_id': 4,
          'birthdate': '2016-09-12',
          'about': 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.',
          'name': 'User 5',
          'created_at': '2017-10-17T18:06:11.481Z',
          'updated_at': '2017-10-17T18:06:11.481Z',
          'url': 'http://localhost:3000/users/106.json',
          'city': {
            'id': 118,
            'name': 'Tønder'
          },
          'target': {
            'id': 4,
            'name': 'Nothing'
          }
        },
        {
          'id': 107,
          'email': 'user_6@example.com',
          'city_id': 120,
          'target_id': 1,
          'birthdate': '1992-10-07',
          'about': 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.',
          'name': 'User 6',
          'created_at': '2017-10-17T18:06:11.614Z',
          'updated_at': '2017-10-17T18:06:11.614Z',
          'url': 'http://localhost:3000/users/107.json',
          'city': {
            'id': 120,
            'name': 'Juelsminde'
          },
          'target': {
            'id': 1,
            'name': 'Friends'
          }
        },
        {
          'id': 108,
          'email': 'user_7@example.com',
          'city_id': 117,
          'target_id': 4,
          'birthdate': '2009-03-22',
          'about': 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.',
          'name': 'User 7',
          'created_at': '2017-10-17T18:06:11.749Z',
          'updated_at': '2017-10-17T18:06:11.749Z',
          'url': 'http://localhost:3000/users/108.json',
          'city': {
            'id': 117,
            'name': 'Tårnby'
          },
          'target': {
            'id': 4,
            'name': 'Nothing'
          }
        },
        {
          'id': 109,
          'email': 'user_8@example.com',
          'city_id': 36,
          'target_id': 1,
          'birthdate': '1985-12-02',
          'about': 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.',
          'name': 'User 8',
          'created_at': '2017-10-17T18:06:11.883Z',
          'updated_at': '2017-10-17T18:06:11.883Z',
          'url': 'http://localhost:3000/users/109.json',
          'city': {
            'id': 36,
            'name': 'Humlebæk'
          },
          'target': {
            'id': 1,
            'name': 'Friends'
          }
        },
        {
          'id': 110,
          'email': 'user_9@example.com',
          'city_id': 6,
          'target_id': 1,
          'birthdate': '1968-10-30',
          'about': 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.',
          'name': 'User 9',
          'created_at': '2017-10-17T18:06:12.016Z',
          'updated_at': '2017-10-17T18:06:12.016Z',
          'url': 'http://localhost:3000/users/110.json',
          'city': {
            'id': 6,
            'name': 'Esbjerg'
          },
          'target': {
            'id': 1,
            'name': 'Friends'
          }
        },
        {
          'id': 111,
          'email': 'user_10@example.com',
          'city_id': 70,
          'target_id': 1,
          'birthdate': '2000-07-18',
          'about': 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.',
          'name': 'User 10',
          'created_at': '2017-10-17T18:06:12.150Z',
          'updated_at': '2017-10-17T18:06:12.150Z',
          'url': 'http://localhost:3000/users/111.json',
          'city': {
            'id': 70,
            'name': 'Glamsbjerg'
          },
          'target': {
            'id': 1,
            'name': 'Friends'
          }
        },
        {
          'id': 112,
          'email': 'user_11@example.com',
          'city_id': 32,
          'target_id': 3,
          'birthdate': '1981-08-26',
          'about': 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.',
          'name': 'User 11',
          'created_at': '2017-10-17T18:06:12.283Z',
          'updated_at': '2017-10-17T18:06:12.283Z',
          'url': 'http://localhost:3000/users/112.json',
          'city': {
            'id': 32,
            'name': 'Gilleleje'
          },
          'target': {
            'id': 3,
            'name': 'Just looking'
          }
        },
        {
          'id': 113,
          'email': 'user_12@example.com',
          'city_id': 49,
          'target_id': 3,
          'birthdate': '2013-06-26',
          'about': 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.',
          'name': 'User 12',
          'created_at': '2017-10-17T18:06:12.416Z',
          'updated_at': '2017-10-17T18:06:12.416Z',
          'url': 'http://localhost:3000/users/113.json',
          'city': {
            'id': 49,
            'name': 'Hørve'
          },
          'target': {
            'id': 3,
            'name': 'Just looking'
          }
        },
        {
          'id': 114,
          'email': 'user_13@example.com',
          'city_id': 65,
          'target_id': 2,
          'birthdate': '1989-03-25',
          'about': 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.',
          'name': 'User 13',
          'created_at': '2017-10-17T18:06:12.550Z',
          'updated_at': '2017-10-17T18:06:12.550Z',
          'url': 'http://localhost:3000/users/114.json',
          'city': {
            'id': 65,
            'name': 'Haderslev'
          },
          'target': {
            'id': 2,
            'name': 'Dates'
          }
        },
        {
          'id': 115,
          'email': 'user_14@example.com',
          'city_id': 138,
          'target_id': 4,
          'birthdate': '2016-11-14',
          'about': 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.',
          'name': 'User 14',
          'created_at': '2017-10-17T18:06:12.683Z',
          'updated_at': '2017-10-17T18:06:12.683Z',
          'url': 'http://localhost:3000/users/115.json',
          'city': {
            'id': 138,
            'name': 'Viborg'
          },
          'target': {
            'id': 4,
            'name': 'Nothing'
          }
        },
        {
          'id': 116,
          'email': 'user_15@example.com',
          'city_id': 94,
          'target_id': 2,
          'birthdate': '1976-02-09',
          'about': 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.',
          'name': 'User 15',
          'created_at': '2017-10-17T18:06:12.816Z',
          'updated_at': '2017-10-17T18:06:12.816Z',
          'url': 'http://localhost:3000/users/116.json',
          'city': {
            'id': 94,
            'name': 'Rungsted'
          },
          'target': {
            'id': 2,
            'name': 'Dates'
          }
        },
        {
          'id': 117,
          'email': 'user_16@example.com',
          'city_id': 4,
          'target_id': 2,
          'birthdate': '1986-01-15',
          'about': 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.',
          'name': 'User 16',
          'created_at': '2017-10-17T18:06:12.950Z',
          'updated_at': '2017-10-17T18:06:12.950Z',
          'url': 'http://localhost:3000/users/117.json',
          'city': {
            'id': 4,
            'name': 'Kongens Lyngby'
          },
          'target': {
            'id': 2,
            'name': 'Dates'
          }
        },
        {
          'id': 118,
          'email': 'user_17@example.com',
          'city_id': 38,
          'target_id': 4,
          'birthdate': '1997-10-26',
          'about': 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.',
          'name': 'User 17',
          'created_at': '2017-10-17T18:06:13.084Z',
          'updated_at': '2017-10-17T18:06:13.084Z',
          'url': 'http://localhost:3000/users/118.json',
          'city': {
            'id': 38,
            'name': 'Hundested'
          },
          'target': {
            'id': 4,
            'name': 'Nothing'
          }
        },
        {
          'id': 119,
          'email': 'user_18@example.com',
          'city_id': 16,
          'target_id': 3,
          'birthdate': '2016-06-03',
          'about': 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.',
          'name': 'User 18',
          'created_at': '2017-10-17T18:06:13.218Z',
          'updated_at': '2017-10-17T18:06:13.218Z',
          'url': 'http://localhost:3000/users/119.json',
          'city': {
            'id': 16,
            'name': 'Ringsted'
          },
          'target': {
            'id': 3,
            'name': 'Just looking'
          }
        },
        {
          'id': 120,
          'email': 'user_19@example.com',
          'city_id': 26,
          'target_id': 3,
          'birthdate': '2016-01-25',
          'about': 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.',
          'name': 'User 19',
          'created_at': '2017-10-17T18:06:13.352Z',
          'updated_at': '2017-10-17T18:06:13.352Z',
          'url': 'http://localhost:3000/users/120.json',
          'city': {
            'id': 26,
            'name': 'Herning'
          },
          'target': {
            'id': 3,
            'name': 'Just looking'
          }
        }
      ],
      newUsers: [],
      onlineUsers: [],
      showModal: false
    }
  },
  mounted () {
    // var axios = require('axios')
    // axios.get('http://jsoneditoronline.org/?id=b29785a0773ad16d2885226f1166904c')
    //   .then((res) => {
    //     console.log(res)
    //   })
    //   .catch((err) => {
    //     console.log(err)
    //   })
    this.newUsers = this.users.slice(0, 8)
    this.onlineUsers = this.users.slice(4, 20)
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="sass" scoped>
</style>
