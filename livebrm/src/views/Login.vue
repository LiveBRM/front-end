<template>
    <div id="login" class="rounded bg-light login">
      <form id="form">
        <div class="form-group">
          <label for="usernameInput">Username</label>
          <input v-model="user" type="username" class="form-control" id="usernameInput" aria-describedby="userHelp" placeholder="Enter username">
          <small id="userHelp" class="form-text text-muted">We'll never share your email with anyone else.</small>
        </div>
        <div class="form-group">
          <label for="exampleInputPassword1">Password</label>
          <input v-model="password" type="password" class="form-control" id="exampleInputPassword1" placeholder="Password">
        </div>
        <div class="form-group form-check">
          <input type="checkbox" class="form-check-input" id="emailCheck">
          <label class="form-check-label" for="emailCheck">Remember email address</label>
        </div>
        <button type="submit" class="btn btn-primary mb-2">Login</button>
        <br>
        <router-link to="/register">Don't have an account?</router-link>
      </form>
    </div>
</template>

<script>
export default {
  name: "login",
  data () {
    return {
      user: '',
      password: '',
    }
  },
  methods: {
    //http requests go here
  }
};
</script>


<!-- Add "scoped" attribute to limit CSS to this component only -->
<style>
/* Extra small devices (phones, 600px and down) */
@media only screen and (max-width: 600px) {
  .login {
    margin: 0 auto;
    height: 50%;
    width: 95%;
    padding: 30px 30px;
  }
}

/* Small devices (portrait tablets and large phones, 600px and up) */
@media only screen and (min-width: 600px) {
  .login {
    margin: 0 auto;
    height: 50%;
    width: 70%;
    padding: 30px 30px;
  }
}

/* Medium devices (landscape tablets, 768px and up) */
@media only screen and (min-width: 768px) {
  .login {
    margin: 0 auto;
    height: 40%;
    width: 50%;
    padding: 30px 30px;
  }
}

/* Large devices (laptops/desktops, 992px and up) */
@media only screen and (min-width: 992px) {
  .login {
    margin: 0 auto;
    height: 35%;
    width: 40%;
    padding: 30px 30px;
  }
}

/* Extra large devices (large laptops and desktops, 1200px and up) */
@media only screen and (min-width: 1200px) {
.login {
    margin: 0 auto;
    height: 30%;
    width: 30%;
    padding: 30px 30px;
  }
}

#form{
  margin: auto;
}
</style>
