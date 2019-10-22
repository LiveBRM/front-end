<template>
  <div class="container">
    <div
      id="businessDetails"
      class="rounded bg-light login"
      style="width: 100%; max-width: 700px"
    >
      <div class="mb-3">
        <h3>Create Account</h3>
      </div>
      <form id="form">
        <div class="form-group">
          <div class="row align-items-center">
            <div class="col-sm-4 col-form-label formLabel">
              <label for="commmonNameInput">Business Common Name</label>
            </div>
            <div class="col">
              <input
                v-model="common_name"
                type="username"
                class="form-control"
                id="commonNameInput"
                aria-describedby="userHelp"
                placeholder="Awesome DJ Company"
              />
            </div>
          </div>
          <div class="row align-items-center">
            <div class="col-sm-4 col-form-label formLabel">
              <label for="legal_name">Business Legal Name</label>
            </div>
            <div class="col">
              <input
                v-model="legal_name"
                type="username"
                class="form-control"
                id="legal_name"
                placeholder="Awesome DJ Company, LLC"
              />
            </div>
          </div>
        </div>
        <div class="form-group">
          <div class="row align-items-center">
            <div class="col-sm-4 col-form-label formLabel">
              <label for="commmonNameInput">Contact Email</label>
            </div>
            <div class="col">
              <input
                v-model="contact_email"
                type="email"
                class="form-control"
                id="email"
                placeholder="contact@awesomedjcompany.com"
              />
            </div>
          </div>
          <div class="row align-items-center">
            <div class="col-sm-4 col-form-label formLabel">
              <label for="phoneNumber">Contact Phone</label>
            </div>
            <div class="col">
              <input
                v-model="phone_number"
                type="phoneNumber"
                class="form-control"
                id="phoneNumber"
                placeholder="(555) 555-1234"
              />
            </div>
          </div>
        </div>
        <div class="form-group">
          <label for="address1">Address</label>
          <input
            v-model="address_line_one"
            type="address"
            class="form-control"
            id="address1"
            placeholder="Address Line 1"
          />
          <input
            v-model="address_line_two"
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
                v-model="province"
                type="state"
                class="form-control"
                id="province"
                placeholder="State/Province"
              />
            </div>
          </div>
          <div class="row mt-2">
            <div class="col">
              <input
                v-model="postal_code"
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
      common_name: "",
      legal_name: "",
      address_line_one: "",
      address_line_two: "",
      city: "",
      province: "",
      postal_code: "",
      country: "",
      contact_email: "",
      phone_number: "",
    };
  },
  methods: {
    checkActive: function(){
      if ( $('#email').is(":focus")) {
        //send HTTP request to see if it's taken
      }
    }
  },
  updated() {
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