<template>
  <div class="container mb-5">
    <div class="wrapper">
      <ol class="ProgressBar">
        <li class="ProgressBar-step is-current">
          <svg class="ProgressBar-icon"><use xlink:href="#checkmark-bold"/></svg>
          <span class="ProgressBar-stepLabel"> Business Info</span>
        </li>
        <li class="ProgressBar-step">
          <svg class="ProgressBar-icon"><use xlink:href="#checkmark-bold"/></svg>
          <span class="ProgressBar-stepLabel">Admin User</span>
        </li>
        <li class="ProgressBar-step">
          <svg class="ProgressBar-icon"><use xlink:href="#checkmark-bold"/></svg>
          <span class="ProgressBar-stepLabel">Create Regular User</span>
        </li>
      </ol>
    </div>
  </div>
</template>

<script>

export default {
  name: "progressCircles",
  data() {
    return {
      step: 1
    };
  },
  methods: {
    
  }
};
</script>

<style scoped>
.ProgressBar {
  margin: 0 auto;
  padding: 2em 0 3em;
  list-style: none;
  position: relative;
  display: flex;
  justify-content: space-between;
}

.ProgressBar-step {
  text-align: center;
  position: relative;
  width: 100%;
}
.ProgressBar-step:before, .ProgressBar-step:after {
  content: "";
  height: 0.5em;
  background-color: #9f9fa3;
  position: absolute;
  z-index: 1;
  width: 100%;
  left: -50%;
  top: 50%;
  -webkit-transform: translateY(-50%);
          transform: translateY(-50%);
  transition: all 0.25s ease-out;
}
.ProgressBar-step:first-child:before, .ProgressBar-step:first-child:after {
  display: none;
}
.ProgressBar-step:after {
  background-color: #00637c;
  width: 0%;
}
.ProgressBar-step.is-complete + .ProgressBar-step.is-current:after, .ProgressBar-step.is-complete + .ProgressBar-step.is-complete:after {
  width: 100%;
}

.ProgressBar-icon {
  width: 1.5em;
  height: 1.5em;
  background-color: #9f9fa3;
  fill: #9f9fa3;
  border-radius: 50%;
  padding: 0.5em;
  max-width: 100%;
  z-index: 10;
  position: relative;
  transition: all 0.25s ease-out;
}
.is-current .ProgressBar-icon {
  fill: #00637c;
  background-color: #00637c;
}
.is-complete .ProgressBar-icon {
  fill: #dbf1ff;
  background-color: #00637c;
}

.ProgressBar-stepLabel {
  display: block;
  text-transform: uppercase;
  color: #9f9fa3;
  position: absolute;
  padding-top: 0.5em;
  width: 100%;
  transition: all 0.25s ease-out;
}
.is-current > .ProgressBar-stepLabel, .is-complete > .ProgressBar-stepLabel {
  color: #00637c;
}

.wrapper {
  font-size: 16px;
}
</style>