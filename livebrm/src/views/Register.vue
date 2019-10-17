<template>
  <div>
    <progressCircles :stepNum="step"></progressCircles>
    <router-view></router-view>
  </div>
</template>

<script>
import progressCircles from "@/components/RegisterProgress.vue";

export default {
  name: "register",
  data() {
    return {
      email: "",
      user: "",
      password: "",
      confirmPassword: "",
      step: ""
    };
  },
  created(){
    this.step = this.$route.path;
    console.log(this.step);
  },
  updated() {
    this.step = this.$route.path;
    console.log(this.step);
  },
  components: {
    progressCircles
  }
};
</script>