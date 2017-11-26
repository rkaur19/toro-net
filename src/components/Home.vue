<template background=".\CSUDH BG.png">
  <link rel="shortcut icon" type="image/x-icon" href="favicon.ico" />
  <div class="container" v-if="this.$store.state.user.displayName">
<<<<<<< HEAD
    <div id="navBar">
        <ul>
          <li><div style="margin: auto; display: block;background-color: transparent;"><img src="logo.jpg" alt="{ToRoNeT}" style="width:50px;height:50px;"></div></li>
          <li><div id="sBar"> <input type="text" name="search" placeholder="Search.."> </div></li>
          <div style="float: right;">
              <li class="dropdown">
                  <a href="javascript:void(0)" class="dropbtn"><i class="fa fa-user" aria-hidden="true" style="font-size:24px"></i></a>
                  <div class="dropdown-content">
                      <a href="#">Friends</a>
                      <a href="#">Link 2</a>
                      <a href="#">Logout</a>
                  </div>
              </li>
              <li><a href="#news"><i class="fa fa-globe" aria-hidden="true" style="font-size:24px"></i></a></li>

              <li class="dropdown"><a href="javascript:void(0)"><i class="fa fa-cog" aria-hidden="true" style="font-size:24px"></i></a>
                  <div class="dropdown-content">
                      <a href="#">Change Stuff</a>
                      <a href="#">?</a>
                      <a href="#">?</a>
                  </div>
              </li>
          </div>
        </ul>
      </div>
        <div id="background1">
          <h1>Welcome to Toro-Net</h1>
          <br>
          <form action="/html/tags/html_form_tag_action.cfm" method="post">
          <textarea name="comments" id="comments" style="width:55%;height:150px;padding:2%;font-size:1.2em;background:url('http://www.oneequalworld.com/wp-content/uploads/2017/02/shutterstock_201120113.jpg');">
          What's on your mind?

          Tell us about your wonderful adventures!

          :) </textarea>
          <br>
          <input type="submit" value="Mail it!">

          <br>
          <br>
          <br>
        </div>
=======
    <h4>Welcome {{this.$store.state.user.displayName}}! What's happening?</h4>
    <br>
    <div class="row">
    <div class="col-xs-1"></div>
    <div class="col-sm-7" >
    <div class="form-group">
      <input type="text" class="form-control" id="title" placeholder="Title" v-model="title">
    </div>
    <div class="form-group">
      <textarea class="form-control" id="body" rows="5" placeholder="Write your thoughts here..." v-model="body">
      </textarea>
    </div>
    <button class="btn btn-primary" @click="addPost()">Post!</button>
    <hr>
    </div>
    <div class="col-sm-1"></div>
    <div class="col-sm-3" style="background-color:lavenderblush;">
    <div class="container-fluid container-scroll">
  <div class="row columns">
    <div class="col-md-2">Field 1</div>
    <div class="col-md-2">Field 2</div>
    <div class="col-md-2">Field 3</div>
    <div class="col-md-2">Field 4</div>
  </div>
</div>

<div class="container-fluid container-scroll">
  <div class="row columns">
    <div class="col-md-2">Field 1</div>
    <div class="col-md-2">Field 2</div>
    <div class="col-md-2">Field 3</div>
    <div class="col-md-2">Field 4</div>
  </div>
</div>

<div class="container-fluid container-scroll">
  <div class="row">
    <div class="col-md-2">Field 1</div>
    <div class="col-md-2">Field 2</div>
    <div class="col-md-2">Field 3</div>
    <div class="col-md-2">Field 4</div>
  </div>
</div>
    </div>
</div>
  <div class="row">
  <div class="col-sm-1"></div>
  <div class="col-sm-7" >
  <div class="form-group">
    <input type="text" class="form-control" id="title" placeholder="Title" v-model="title">
  </div>
  <div class="form-group">
    <textarea class="form-control" id="body" rows="5" placeholder="Write your thoughts here..." v-model="body">
    </textarea>
  </div>
  <button class="btn btn-primary" @click="addPost()">Post!</button>
  <hr>
  </div>

  <div class="col-sm-3"></div>
</div>
  </div>

>>>>>>> 317b065c85b985b1f4c41979e152af673884092e
  <div class="container" v-else>
    <h4>You must login to access Toro-Net!</h4> //changes made here
  </div>
</template>

<script>
export default {
  name: 'Home',
  data() {
    return {
      // date: Date.now(),
      // username: this.$store.user.username,
      // email: this.$store.user.email,
      // displayName: this.$store.user.displayName,
      // Are the above data to be included here?
      // I think not, since the data would be passed around more times
      // than is probably necessary... $store is accessible globally
      // throughout the app after all.
      title: '',
      body: ''
    };
  },
  methods: {
    addPost() {
      this.$store.dispatch('addPost', this.$store.state.posts)
    }
  },
  mounted() {
    this.$store.dispatch('getPosts')
    this.$store.dispatch('getUser')
  },
}
</script>

<<<<<<< HEAD
<style scoped>

body {
    background-color: rgb(196, 156, 140);
    background-image: url("https://www.csudh.edu/Assets/Global/backgrounds/Background-LSU1-yellow.jpg");
    background-repeat: no-repeat;
    margin-left: 3%;
    margin-right: 3%;
    background-position: center;
    background-size:cover;
}

#background1{
    color:#333;
   /* opacity: .5; */
}



ul {
    list-style-type: none;
    margin: 0;
    padding: 0;
    overflow: hidden;
    background-color: #860038;
}

li {
    float: left;
}

li a, .dropbtn {
    display: inline-block;
    color: white;
    text-align: center;
    padding: 14px 16px;
    text-decoration: none;
}

li a:hover, .dropdown:hover .dropbtn {
    background-color: red;
}

li.dropdown {
    display: inline-block;
}

.dropdown-content {
    display: none;
    position: absolute;
    background-color: #f9f9f9;
    min-width: 160px;
    box-shadow: 0px 8px 16px 0px rgba(0,0,0,0.2);
    z-index: 1;
}

.dropdown-content a {
    color: black;
    padding: 12px 16px;
    text-decoration: none;
    display: block;
    text-align: left;
}

.dropdown-content a:hover {background-color: #f1f1f1}

.dropdown:hover .dropdown-content {
    display: block;
}

input[type=text] {
    width: 100%;
    -webkit-transition: width 0.4s ease-in-out;
    transition: width 0.4s ease-in-out;
}

/* When the input field gets focus, change its width to 100% */
input[type=text]:focus {
    width: 150%;
}

div #sBar{
    text-align: center;
    padding: 14px 16px;
=======
<style>
@media (min-width: 992px) {
  .container-scroll {
    overflow-x: auto;
  }
  .container-scroll .columns-16 {
    width: 133.33333333vw;  /* = 100vw * 16/12 */
  }
  .container-scroll .columns-24 {
    width: 200vw;  /* = 100vw * 24/12 */
  }
  .container-scroll .col-md-2 {
    width: 16.66666667vw !important;
  }
}

.container-scroll > .row {
  margin-top: 24px;
}
.container-scroll > .row > .col-md-2 {
  font-weight: bold;
  text-align: center;
>>>>>>> 317b065c85b985b1f4c41979e152af673884092e
}

</style>
