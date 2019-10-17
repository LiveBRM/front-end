<template>
  <div id="businessDetails" class="rounded bg-light login">
    <div class="mb-3">
      <h3>Create Account</h3>
    </div>      
    <form id="form">
    <div class="form-group">
      <label for="userName">Admin Username</label>
        <input
          v-model="adminUser"
          type="username"
          class="form-control"
          id="username"
          placeholder="Enter username"
        />
      </div>
      <div class="form-group">
        <label for="userName">Admin Password</label>
        <input
          v-model="adminUser"
          type="username"
          class="form-control"
          id="username"
          placeholder="Enter username"
        />
      </div>
      <div class="form-group form-inline">
        <label for="firstName">Name</label>
        <input
          v-model="firstName"
          type="firstName"
          class="form-control"
          id="firstName"
          placeholder="John"
        />
        <input
          v-model="lastname"
          type="lastName"
          class="form-control mt-2"
          id="lastName"
          placeholder="Doe"
        />
      </div>
      <div class="form-group">
        <label for="email">Email</label>
        <input
          v-model="email"
          type="email"
          class="form-control"
          id="email"
          placeholder="Contact email"
        />
      </div>
      <div class="form-group">
        <label for="phoneNumber">Phone number</label>
        <input
          v-model="phoneNumber"
          type="phoneNumber"
          class="form-control"
          id="phoneNumber"
          placeholder="1(800)-000-0000"
        />
      </div>
      <div class="row">
        <div class="col">
          <router-link class="btn btn-primary previous" to="/register/1"
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
      email: "",
    };
  }
};
</script>
