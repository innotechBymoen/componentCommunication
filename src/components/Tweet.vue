<template>
  <div>
    <p v-on:click="notifyParent">{{ author }}</p>
    <p v-on:click="makeRed">{{ content }}</p>
  </div>
</template>

<script>
export default {
  name: "Tweet",
  props: {
    author: {
      type: String,
      required: true
    }
  },
  methods: {
    makeRed: function() {
      document.body.style.background = "red";
    },
    notifyParent: function() {
      this.$emit("myCustomEvent", this.author);
    }
  },
  data: function() {
    return {
      content: "This is the tweet content"
    };
  }
};
</script>

<style scoped>
div {
  margin: 10vh 0;
  border: 1px solid black;
  background: white;
  box-shadow: 5px 5px 5px grey;
}
</style>