<template>
  <div class="register">
    <form @submit.prevent="addEditUser">
      <h1>Let's get you onto the cheapest deal</h1>
      <Message v-bind:message="this.texts.currentSupply"/>
      <label for="postcode">Postcode</label>
      <div class="form-group">
        <input type="text" name="postode" />
        <button type="button">Find Address</button>
      </div>
      <CecSelect />
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
import CecSelect from "@/shared/cecSelect/CecSelect";
export default {
  name: "Register",
  components: {
    Message,
    CecSelect
  },
  data() {
    return {
      texts: texts.data
    };
  },
  methods: {
    addEditUser() {
      console.log('addEditUser');
    }
  }
};
</script>
<style lang="scss">
</style>