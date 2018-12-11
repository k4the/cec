<template>
  <div class="sub-title mbBig">
    <h3>{{this.subTitle.title}}</h3>
    <p v-if="this.subTitle.message">{{this.subTitle.message}}</p>
  </div>
</template>
<script>
export default {
  name: "SubTitle",
  props: ['subTitle'],
  data() {return { }}
};
</script>