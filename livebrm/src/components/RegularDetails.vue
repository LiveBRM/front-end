<template>
  <div class="container">
    <div
      id="businessDetails"
      class="rounded bg-light login"
      style="width: 100%; max-width: 700px"
    >
      <div class="mb-3">
        <h3>Create Regular User</h3>
      </div>
      <form id="form">
        <div class="form-group">
          <div class="row align-items-center">
            <div class="col-sm-3 col-form-label formLabel">
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
          <div class="col-sm-3 col-form-label formLabel">
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
          <div class="col-sm-3 col-form-label formLabel">
            <label for="username">Username</label>
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
          <div class="col-sm-3 col-form-label formLabel">
            <label for="password">Password</label>
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
          <div class="col-sm-3 col-form-label formLabel">
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
            <router-link class="btn btn-link previous" to="/register/2"
              >Back</router-link
            >
          </div>
          <div class="col">
            <button class="btn btn-primary advance">Submit</button>
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
      reg_f_name: "",
      reg_k_name: "",
      reg_email: "",
      reg_username: "",
      reg_password: "",
      reg_password_confirm: ""
    };
  },
  methods: {
    sendRequest: function(){
      http.request({
        url: "https://httpbin.org/post",
          method: "POST",
          headers: { "Content-Type": "application/json" },
          content: JSON.stringify({
            reg_f_name: "",
            reg_k_name: "",
            reg_email: "",
            reg_username: "",
            reg_password: "",
            reg_password_confirm: ""
          })
      }).then(response => {
        this.result = response.content.toJSON();
        }, error => {
        console.error(error);
      });
    }
  },
  updated(){
    this.checkActive();
  }
};
</script>

<style scoped>
/* large devices (portrait tablets and large phones, 576px and up) */
@media only screen and (min-width: 576px) {
  .formLabel {
    text-align: right!important;
  }
}
</style>