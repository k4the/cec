<template>
  <div class="register">
    <form>
      <h1>Let's get you onto the cheapest deal</h1>
      <SubTitle v-bind:sub-title="this.subTitles.currentSupply"/>
      <SubTitle v-bind:sub-title="this.subTitles.energySupplier"/>
      <SubTitle v-bind:sub-title="this.subTitles.tellUs"/>
    </form>
    <div class="sidebar">
        <h2>How it works</h2>
    </div>
  </div>
</template>

<script>
import './register.scss';
import * as subTitles from './data';
import SubTitle from "@/register/SubTitle";
export default {
  name: "Register",
  components: {
    SubTitle
  },
  data() {
    return {
      subTitles: subTitles.data
    };
  }
};
</script>
<style lang="scss">
</style>