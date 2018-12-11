<template>
  <div class="register">
    <form>
      <h1>Let's get you onto the cheapest deal</h1>
      <Message v-bind:message="this.texts.currentSupply"/>
      <label for="postcode">Postcode</label>
      <div class="form-group">
        <input type="text" name="postode" />
        <button type="button">Find Address</button>
      </div>
      <Message v-bind:message="this.texts.energySupplier"/>
      <Message v-bind:message="this.texts.tellUs"/>
      <Message v-bind:message="this.texts.addressFirst" v-bind:message-class="'plain'"/>
    </form>
    <div class="sidebar">
        <h2>How it works</h2>
    </div>
  </div>
</template>

<script>
import './register.scss';
import * as texts from './data';
import Message from "@/register/Message";
export default {
  name: "Register",
  components: {
    Message
  },
  data() {
    return {
      texts: texts.data
    };
  }
};
</script>
<style lang="scss">
</style>