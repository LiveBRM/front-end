<template>
  <div class="container">
    <div
      id="businessDetails"
      class="rounded bg-light login"
      style="width: 100%; max-width: 700px"
    >
      <div class="mb-3">
        <h3>Create Admin User</h3>
      </div>
      <form id="form">
        <div class="form-group">
          <div class="row align-items-center">
            <div class="col-sm-3 col-form-label">
              <label for="firstName">Name</label>
            </div>
            <div class="col">
              <input
                v-model="firstName"
                type="text"
                class="form-control"
                id="firstName"
                placeholder="John"
              />
            </div>
            <div class="col">
              <input
                v-model="lastname"
                type="text"
                class="form-control"
                id="lastName"
                placeholder="Doe"
              />
            </div>
          </div>
        </div>
        <div class="row align-items-center">
          <div class="col-sm-3 col-form-label">
            <label for="email">Email</label>
          </div>
          <div class="col-sm-9">
            <input
              v-model="email"
              type="email"
              class="form-control"
              id="email"
              placeholder="Email"
            />
          </div>
        </div>
        <div class="row align-items-center">
          <div class="col-sm-3 col-form-label">
            <label for="username">Admin Username</label>
          </div>
          <div class="col-sm-9">
            <input
              v-model="commonName"
              type="username"
              class="form-control"
              id="username"
              placeholder="Username"
            />
          </div>
        </div>
        <div class="row align-items-center">
          <div class="col-sm-3 col-form-label">
            <label for="password">Admin Password</label>
          </div>
          <div class="col-sm-9">
            <input
              v-model="adminPassword"
              type="password"
              class="form-control"
              id="password"
              placeholder="Password"
            />
          </div>
        </div>
        <div class="row align-items-center">
          <div class="col-sm-3 col-form-label">
            <label for="confirmPassword">Confirm Password</label>
          </div>
          <div class="col-sm-9">
            <input
              v-model="adminConfirmPassword"
              type="password"
              class="form-control"
              id="confirmPassword"
              placeholder="Confirm Password"
            />
          </div>
        </div>
        <div class="row align-items-center mt-2">
          <div class="col">
            <router-link class="btn btn-link previous" to="/register/1"
              >Back</router-link
            >
          </div>
          <div class="col">
            <button class="btn btn-primary advance">Next</button>
          </div>
        </div>
        <br />
      </form>
    </div>
  </div>
</template>

<script>
export default {
  name: "adminDetails",
  data() {
    return {
      adminUser: "",
      adminPassword: "",
      adminConfirmPassword: "",
      firstName: "",
      lastname: "",
      email: ""
    };
  },
  methods: {
    checkActive: function(){
      if ( $('#email').is(":focus")) {
        //send HTTP request to see if it's taken
      }
    }
  },
  updated(){
    this.checkActive();
  }
};
</script>
