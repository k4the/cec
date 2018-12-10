<template>
  <div class="register">
    <form>
      <h1>Let's get you onto the cheapest deal</h1>
      <div class="sub-title">
        <h2>Your current supply</h2>
        <p>Give us your details and we'll use a comparison to check your current tariff</p>
      </div>
    </form>
    <div class="sidebar">
        <h1>How it works</h1>
    </div>
  </div>
</template>

<script>
import './register.scss';
import * as subTitles from './data';
console.log(subTitles.data.currentSupply);
export default {
  name: "Register",
  data() {
    return {};
  }
};
</script>
<style lang="scss">
</style>