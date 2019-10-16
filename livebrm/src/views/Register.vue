<template>
    <div id="register" class="rounded bg-light login">
      <div class="mb-3">
          <h3>Create Account</h3>
        </div>
      <form id="form">
        <div class="form-group">
          <label for="emailInput">Email</label>
          <input v-model="emailf" type="username" class="form-control" id="emailInput" aria-describedby="userHelp" placeholder="Enter email">
          <small id="userHelp" class="form-text text-muted">We'll never share your email with anyone else.</small>
        </div>
        <div class="form-group">
          <label for="userInput">Username</label>
          <input v-model="user" type="username" class="form-control" id="userInput" placeholder="Enter username">
        </div>
        <div class="form-group">
          <label for="password">Password</label>
          <input v-model="password" type="password" class="form-control" id="password" placeholder="Password">
        </div>
        <div class="form-group">
          <input v-model="confirmPassword" type="password" class="form-control" id="confirmPassword" placeholder="Confirm Password">
        </div>
        <button type="submit" class="btn btn-primary mb-1">Create Account</button>
        <br>
        <router-link to="/login">Already have an account? Login here</router-link>
      </form>
    </div>    
</template>

<script>
export default {
  name: "register",
  data () {
    return {
      email: '',
      user: '',
      password: '',
      confirmPassword: '',
    }
  } 
};
</script>
