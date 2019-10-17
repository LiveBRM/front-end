<template>
  <div>
    <progressCircles></progressCircles>
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
      confirmPassword: ""
    };
  },
  components: {
    progressCircles
  }
};
</script>