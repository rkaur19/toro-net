<template>
  <div id="app">
    <!-- changes at 2:35pm Nov. 21st -->
    <!-- <div class="container">
       <form class="" action="index.html" method="post">
            <div class="well">
               <h4>Add user here</h4>
               <div class="form-group">
                    <label class="pull-left" for="">First Name</label>
                    <input type="text" class="form-control" name="" placeholder="first name comes here" value="">
                    <button class="btn btn-primary" type="button" name="button">Submitttt</button>
               </div>
            </div>
       </form>
    </div> -->

    <!-- changes at 2:35pm Nov. 21st -->

 <!-- Navigation bar, fixed top -->
    <nav class="navbar navbar-expand-lg navbar-inverse bg-light fixed-top">
      <a class="navbar-brand" href="index.html">Toro-Net</a>

      <!-- responsive button -->
      <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
        <span class="navbar-toggler-icon"></span>
      </button>


            <!-- content collapses in smaller screen size -->
      <div class="collapse navbar-collapse" id="navbarSupportedContent">
        <ul class="navbar-nav mr-auto">

          <!-- home page -->
          <li class="nav-item active">
            <a class="nav-link" href="index.html"><span class="fa fa-home"></span> Home <span class="sr-only">(current)</span></a>
          </li>

          <!-- Sign in button  -->
         <li class="nav-item">
           <a class="nav-link" href="#"> <span class="fa fa-user-plus"></span> Sign up </a>
         </li>

           <!-- log in button  -->
          <li class="nav-item">
            <a class="nav-link" href="#"> <span class="fa fa-sign-in"></span> Login </a>
          </li>



          <!-- no dropdown  needed -->
          <!-- <li class="nav-item dropdown">
            <a class="nav-link dropdown-toggle" href="#" id="navbarDropdown" role="button" data-toggle="dropdown" aria-haspopup="true" aria-expanded="false">
              Dropdown
            </a>
            <div class="dropdown-menu" aria-labelledby="navbarDropdown">
              <a class="dropdown-item" href="#">Action</a>
              <a class="dropdown-item" href="#">Another action</a>
              <div class="dropdown-divider"></div>
              <a class="dropdown-item" href="#">Something else here</a>
            </div>
          </li> -->
          <!-- <li class="nav-item">
            <a class="nav-link disabled" href="#">Disabled</a>
          </li> -->
        </ul>

        <form class="form-inline my-2 my-lg-0">
          <input class="form-control mr-sm-2" type="search" placeholder="Search" aria-label="Search">
          <button class="btn btn-outline-success my-2 my-sm-0" type="submit">Search</button>
        </form>
      </div>
    </nav>


 <br>
 <br>
 <br>

<!-- header -->
 <!-- <header class="jumbotron">
         <div class="container">
             <div class="row row-header">
                 <div class="col-12 col-sm-8">
                     <h1>Social network for csudh</h1>
                     <p> share and inspire each other !</p>
                 </div>
                 <div class="col col-sm">
                 </div>
             </div>
         </div>
     </header> -->

  <!-- changes at 2:35pm Nov. 21st -->
  <!-- body -->
  <div class="container">

           <hr>
          <router-link to="/">Home</router-link>
          <a v-if="!this.$store.state.user.displayName" href="/register" @click="register">Register</a>
          <a v-if="this.$store.state.user.displayName" href="/logout" @click="logout">Logout</a>
          <router-link v-else to="/login">Login</router-link>
          <h1>{{ title }}</h1>
          <hr />
          <router-view />


  </div>

<div class="">
  <br>
  <br>
  <br>
  <br>
  <br>
  <br>
  <br>
  <br>
  <br>
  <br>
  <br>
  <br>
  <br>
  <br>
  <br>
</div>

 <!-- footer  -->

    <footer class="footer">
          <div class="container">
              <div class="row">
                  <div class="col-5 offset-1 col-sm-2">
                      <h5>Links</h5>
                      <ul class="list-unstyled">
                          <li><a href="./index.html">Home</a></li>
                          <li><a href="./aboutus.html">About</a></li>
                          <!-- <li><a href="#"></a></li> -->
                          <li><a href="#">Contact</a></li>
                      </ul>
                  </div>
                  <div class="col-6 col-sm-5">
                      <h5>Our Address</h5>
                      <address>
                    1000 E Victoria St<br>
                    Carson, CA 90747<br>
                    United States<br>
                    <i class="fa fa-phone fa-lg"></i>: +1 310 243 3696<br>
                    <i class="fa fa-fax fa-lg"></i>: +1 310 243 3696<br>
                    <i class="fa fa-envelope fa-lg"></i>: <a href="mailto:awang26@toromail.csudh.edu">Email Us</a> <br>
                 </address>
                  </div>
                  <div class="col-sm align-self-center">
                      <div style="text-align:center">
                          <a class="btn btn-social-icon btn-google-plus" href="http://google.com/+"><i class="fa fa-google-plus"></i></a>
                          <a class="btn btn-social-icon btn-facebook" href="http://www.facebook.com/profile.php?id="><i class="fa fa-facebook"></i></a>
                          <a class="btn btn-social-icon btn-linkedin" href="http://www.linkedin.com/in/"><i class="fa fa-linkedin"></i></a>
                          <a class="btn btn-social-icon btn-twitter" href="http://twitter.com/"><i class="fa fa-twitter"></i></a>
                          <a class="btn btn-social-icon btn-youtube" href="http://youtube.com/"><i class="fa fa-youtube"></i></a>
                          <a class="btn btn-social-icon" href="mailto:"><i class="fa fa-envelope-o"></i></a>
                      </div>
                  </div>
             </div>
             <div class="row justify-content-center">
                  <div class="col-auto">
                      <p>© Copyright 2017 CSUDH Frontend Team</p>
                  </div>
             </div>
          </div>
      </footer>




  </div>

</template>

<script>
export default {
  name: 'app',
  data () {
    return {
      title: 'Toro--Net'
    }
  },
  methods: {
    logout() {
      this.$store.dispatch('logout')
    }
  },
  mounted() {
    this.$store.dispatch('getUser')
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 30px;
}

h1, h2 {
  font-weight: normal;
}

ul {
  list-style-type: none;
  padding: 0;
}

a {
  color: #42b983;
}
</style>
