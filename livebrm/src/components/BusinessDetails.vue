<!--ADD NEW HORIZONTAL FORM ON BOOTSTRAP-->
<template>
  <div class="container">
    <div id="businessDetails" class="rounded bg-light login" style="width: 100%; max-width: 700px">
      <div class="mb-3">
        <h3>Create Account</h3>
      </div>
      <form id="form">
        <div class="form-group">
          <div class="row align-items-center">
            <div class="col-sm-4 col-form-label">
              <label for="commmonNameInput">Business Common Name</label>
            </div>
            <div class="col">
              <input
              v-model="commonName"
              type="username"
              class="form-control"
              id="commonNameInput"
              aria-describedby="userHelp"
              placeholder="Awesome DJ Company"
              />
            </div>
          </div>
          <div class="row align-items-center">
            <div class="col-sm-4 col-form-label">
              <label for="legalName">Business Legal Name</label>
            </div>
            <div class="col">
              <input
              v-model="user"
              type="username"
              class="form-control"
              id="legalName"
              placeholder="Awesome DJ Company, LLC"
              />
            </div>
          </div>    
        </div>
        <div class="form-group">
          <div class="row align-items-center">
            <div class="col-sm-4 col-form-label">
              <label for="commmonNameInput">Contact Email</label>
            </div>
            <div class="col">
              <input v-model="email"
                type="email"
                class="form-control"
                id="email"
                placeholder="contact@awesomedjcompany.com">
            </div>
          </div>
          <div class="row align-items-center">
            <div class="col-sm-4 col-form-label">
              <label for="phoneNumber">Contact Phone</label>
            </div>
            <div class="col">
              <input v-model="phoneNumber"
              type="phoneNumber"
              class="form-control"
              id="phoneNumber"
              placeholder="(555) 555-1234" />
            </div>
          </div>
        </div>
        <div class="form-group">
          <label for="address1">Address</label>
          <input
            v-model="addressLine1"
            type="address"
            class="form-control"
            id="address1"
            placeholder="Address Line 1"
          />
          <input
            v-model="addressLine2"
            type="address"
            class="form-control mt-2"
            id="address2"
            placeholder="Address Line 2"
          />
        </div>
        <div class="form-group">
          <div class="row">
            <div class="col">
              <input
                v-model="city"
                type="city"
                class="form-control"
                id="city"
                placeholder="City"
              />
            </div>
            <div class="col">
              <input
                v-model="stateOrProvince"
                type="state"
                class="form-control"
                id="stateOrProvince"
                placeholder="State/Province"
              />
            </div>
          </div>
          <div class="row mt-2">
            <div class="col">
              <input
                v-model="postalCode"
                type="postalCode"
                class="form-control"
                id="postalCode"
                placeholder="Postal Code"
              />
            </div>
            <div class="col">
              <input
                v-model="country"
                type="country"
                class="form-control"
                id="country"
                placeholder="Country"
              />
            </div>
          </div>
        </div>
        <div class="row align-items-center">
          <div class="col">
            <router-link class="previous" to="/login">
              Back to Login
            </router-link>
          </div>
          <div class="col">
            <router-link class="btn btn-primary advance" to="/register/2/">
              Next
            </router-link>
          </div>
        </div>
        <br />
      </form>
    </div>
  </div>
</template>

<script>
export default {
  name: "businessDetails",
  data() {
    return {
      commonName: "",
      legalName: "",
      addressLine1: "",
      addressLine2: "",
      city: "",
      stateOrProvince: "",
      postalCode: "",
      country: "",
      email: "",
      phoneNumber: "",
      emergencyContactPhone: "",
      normalBusinessPhone: ""
    };
  }
};
</script>
