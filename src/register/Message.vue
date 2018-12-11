<template>
  <div class="message" v-bind:class="{ 'plain': this.isPlain }">
    <h3 v-if="this.message.title">{{this.message.title}}</h3>
    <p v-if="this.message.body">{{this.message.body}}</p>
  </div>
</template>
<script>
export default {
  name: "Message",
  props: ['message', 'messageClass'],
  data() {
    return {
      isPlain: this.getClass()
     }
    },
    methods: {
      getClass() {
        if(this.messageClass) {
          return true;
        } else {
          return false;
        }
      }
    }
};
</script>