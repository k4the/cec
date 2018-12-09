<template>
  <div class="header">
    <div class="logo mr mb">
      <img src="../assets/cec-logo.png" alt="Cheap Energy Club">
    </div>
    <h3 class="mr primary">Already joined? Login</h3>
    <div class="login-header">
      <Login/>
    </div>
  </div>
</template>

<script>
import Login from "@/login/Login";
export default {
  name: "Header",
  components: {
    Login
  },
  data() {
    return {};
  }
};
</script>
<style lang="scss">
.header {
  display: flex;
  flex-direction: column;
  align-items: normal;
  background: white;
  padding: 0;

  @include desktop {
    flex-direction: row;
    align-items: center;
    background: $secondaryLight;
    padding: 0 $defaultPaddingSize;
  }

  .logo {
    cursor: pointer;
    text-align: center;

    @include tablet {
      text-align: left;
    }
  }

  .login-header {
    align-content: flex-end;
    flex: 1;
  }
}
</style>