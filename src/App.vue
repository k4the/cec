<template>
  <div id="app" class="container">
    <div class="header-main-wrapper">
      <Header/>
      <div class="main">
        <router-view/>
      </div>
    </div>
    <Footer/>
  </div>
</template>
<script>
import './app.scss';
import Header from "@/header/Header";
import Footer from "@/footer/Footer";
export default {
  name: "App",
  components: {
    Header,
    Footer
  }
};
</script>
<style lang="scss">
</style>
