<template>
  <div id="app">


 <!-- Navigation bar, fixed top -->
    <nav class="navbar navbar-expand-lg navbar-inverse bg-dark  text-white fixed-top">
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

  <div class="container  bg-light">

           <hr>
          <router-link to="/">Home</router-link>
          <a v-if="!this.$store.state.user.displayName" href="/register" @click="register">Register</a>
          <a v-if="this.$store.state.user.displayName" href="/logout" @click="logout">Logout</a>
          <router-link v-else to="/login">Login</router-link>
          <!-- <h1>{{ title }}</h1> -->
          <hr />
          <router-view />


  </div>

  <div class="container bg-light">
    <div class="row">
        <!-- display information on home page -->
        <div class="col-sm-0 col-lg-8">
            <br>
          <div class="row offset-sm-2">
               <h2>Connect with friends from CSUDH. </h2>
          </div>
          <br>
          <div class="row offset-sm-1">
            <p><span class="fa fa-pencil-square-o fa-3x"></span>  See posts and updates from friends.</p>
          </div>
          <br>
          <div class="row offset-sm-1">
            <p> <span class="fa fa-share-alt-square fa-3x"></span>  Share what's new in your life.</p>
          </div>
          <br>
          <div class="row offset-sm-1">
            <p><span class="fa fa-users fa-3x"></span>  Connect with more...</p>
          </div>





        </div>

      <!-- // sign up form -->
      <div class="form col-sm-12 col-lg-4">
          <h2 class="strong text-left">Join Us Now!</h2>
          <p class="text-left">Fun is on the way...</p>
          <!-- <div class="row">
              <input type="text" name="" value="" placeholder="First Name">
              <input type="text" name="" value="" placeholder="Last Name">
          </div>
          <div class="row">
              <input type="text" name="" value="" placeholder="Mobile number/Email">
          </div>
          <div class="row">
              <input type="text" name="" value="" placeholder="Password">
          </div>
          <div class="row">
              <input type="text" name="" value="" placeholder="Reenter Password">
          </div> -->


          <form class="fomr-horizontal" role="form">
              <div class="form-group row">
                <!-- <label for="name" class="col-sm-3 control-label">Full Name</label> -->
                <!-- first name -->
                  <div class="col-sm-6">
                    <input type="text" class="form-control" placeholder="First name">
                  </div>
                  <!-- <div class="col-sm-1">

                  </div> -->
                  <!-- last name -->
                    <div class="col-sm-6">
                      <input type="text" class="form-control" placeholder="Last name">
                    </div>
              </div>
              <!-- email/ phone number -->
              <div class="form-group row">
                    <!-- <label for="staticEmail" class="col-sm-3 col-form-label">Email/Phone</label> -->
                    <div class="col-sm-12">
                      <input type="email" class="form-control" id="exampleFormControlInput1" placeholder="Email or Phone">
                    </div>
              </div>
              <div class="form-group row">
                <!-- <label for="inputPassword" class="col-sm-3 col-form-label">Password</label> -->
                <div class="col-sm-12">
                  <input type="password" class="form-control" id="inputPassword" placeholder="Password">
                </div>
              </div>
              <div class="form-group row">
                <!-- <label for="inputPassword" class="col-sm-3 col-form-label">Password(Confirm)</label> -->
                <div class="col-sm-12">
                  <input type="password" class="form-control" id="ConfirmPassword" placeholder="Confirm password">
                </div>
              </div>
              <!-- Date of Birth -->
              <!-- <div class="form-control">
                <label for="">Date of Birth</label>
                  <div class="col-sm-12">
                    <input type="date" name="birthdate" value="" class="form-control" placeholder="Date of Birth">

                  </div>
              </div> -->
              <br>
              <!-- radio buttons for genders -->
              <div class="form-group row">
                    <div class="form-check col-sm-3">
                            <label class="form-check-label">
                              <input class="form-check-input" type="radio" name="exampleRadios" id="exampleRadios1" value="option1" checked>
                              <strong>Female</strong>
                            </label>
                    </div>
                    <div class="form-check col-sm-3">
                          <label class="form-check-label">
                            <input class="form-check-input" type="radio" name="exampleRadios" id="exampleRadios2" value="option2">
                            <strong>Male</strong>
                          </label>
                      </div>
              </div>

              <div class="control-group col-12">
                    <!-- Button -->
                    <div class="controls row">
                      <button class="btn btn-primary btn-block">Sign up</button>
                    </div>
             </div>
              <!-- terms -->
              <div class="col-12 text-left font-italic small">
                By clicking Create Account, you agree to our
                <a href="#">Terms</a>
                and that you have read our
                <a href="#">Data Policy</a>
                , including our
                <a href="#">Cookie Use</a>
                . You may receive SMS Notifications from Toro-Net and can opt out at any time.
              </div>


          </form>



      </div>
    </div>




  </div>

<div class="">
  <br>
  <br>
  <br>
  <br>
</div>
<hr>
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
