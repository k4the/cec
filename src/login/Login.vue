<template>
  <form class="login">
    <div class="input-group mr">
      <label for="email" class="mobile-only">Email address</label>
      <input type="email" id="email">
    </div>
    <div class="input-group mr">
      <label for="password" class="mobile-only">Password</label>
      <div class="input-button">
        <input type="password" id="password">
        <button type="button" id="password-button" @click="togglePassword()">
          <i class="far fa-eye" id="password-icon"></i>
        </button>
      </div>
    </div>
    <button id="loginButton" class="btnPrimary">Go</button>
  </form>
</template>

<script>
export default {
  name: "Login",
  data() {
    return {};
  },
  methods: {
    togglePassword() {
      var password = document.getElementById("password");
      var passwordIcon = document.getElementById("password-icon");
      if (password) {
        if (password.getAttribute("type") === "password") {
          password.setAttribute("type", "text");
          passwordIcon.classList.remove("fa-eye");
          passwordIcon.classList.add("fa-eye-slash");
        } else {
          password.setAttribute("type", "password");
          passwordIcon.classList.remove("fa-eye-slash");
          passwordIcon.classList.add("fa-eye");
        }
      }
    }
  }
};
</script>
<style lang="scss">
.login {
  display: flex;
  flex-direction: column;
  justify-content: space-between;

  .input-group {
    margin-bottom: $defaultSize;
  }

  #loginButton {
    width: auto;
    float: none;
  }

  @include desktop {
    flex-direction: row;
    .input-group {
      margin-bottom: 0;
    }

    #loginButton {
      width: auto;
      float: right;
    }
  }
}
</style>