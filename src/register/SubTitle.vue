<template>
  <div class="sub-title">
    <h2>{{title}}</h2>
    <p>{{message}}</p>
  </div>
</template>

<script>
export default {
  name: "SubTitle",
  data() {
    return {
        subTitle: {
            title: null,
            message: null
        }
    };
  }
};
</script>