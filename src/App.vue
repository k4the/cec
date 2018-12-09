<template>
  <div id="app" class="container">
    <Header />
    <router-view class="main" />
  </div>
</template>

<script>
import Header from '@/header/Header'
export default {
  name: 'App',
  components: {
    Header
  }
}
</script>
<style lang="scss">
.container {
  max-width: 990px;
  margin: 0 auto;
  text-align: center;

  .main {
    text-align: left;
    background: white;
    min-height: 200px;
  }
}
</style>
