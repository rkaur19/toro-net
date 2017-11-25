<template>
  <div class="container" v-if="this.$store.state.user.displayName">
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
}

</style>
