<template>
  <header>
    <div class="logo mr mb">
      <img src="../assets/cec-logo.png" alt="Cheap Energy Club">
    </div>
    <h4 class="mr primary">Already joined? Login</h4>
    <div class="login-header">
      <Login/>
    </div>
  </header>
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
header {
  display: flex;
  flex-direction: column;
  align-items: normal;
  background: white;
  padding: $defaultSize $defaultSize 0 $defaultSize;

  @include desktop {
    flex-direction: row;
    align-items: center;
    background: $secondaryLight;
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