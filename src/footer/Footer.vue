<template>
  <footer>
    <nav>
      <a class="footer-link inline">Privacy policy</a>
      <a class="footer-link inline">Terms &amp; conditions</a>
      <a class="footer-link inline">Help/FAQ</a>
    </nav>
    <nav>
      <a class="footer-link">A tool from MoneySavingExpert.com</a>
      <a class="footer-link">Technology Experts MSM</a>
    </nav>
  </footer>
</template>

<script>
export default {
  name: "Footer",
  data() {
    return {};
  }
};
</script>
<style lang="scss">
footer {
  nav {
    margin: 0 auto;
    display: block;
  }

  .footer-link {
    padding: 0 $defaultPaddingVertical;
    color: $neutralDark;
    font-size: smaller;
    display: block;

    .inline {
      display: inline-block;
    }
  }

  .footer-link.inline {
    display: inline-block;
  }

  @include desktop {
    .footer-link {
      display: inline-block;
    }
  }
}
</style>