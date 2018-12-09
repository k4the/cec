<template>
  <div id="app" class="container">
    <div class="header-main-wrapper">
      <Header/>
      <router-view class="main"/>
    </div>
    <Footer/>
  </div>
</template>

<script>
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
.container {
  max-width: 990px;
  margin: 0 auto;
  text-align: center;
  position: relative;
  min-height: 100vh;
  background: white;

  .header-main-wrapper {
    padding-bottom: 4.5rem; /* Footer height */
  }

  .main {
    text-align: left;
    background: white;
    min-height: 200px;
  }

  .footer {
    height: auto;
    background: $secondaryLight;
    padding: $defaultPaddingSize;
    text-align: center;
    position: absolute;
    bottom: 0;
    width: 100%;
  }

  @include desktop {
    .header-main-wrapper {
      padding-bottom: 4.5rem;
    }

    .footer {
      height: 4.5rem;
    }
  }
}
</style>
