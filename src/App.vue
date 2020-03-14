<template>
  <div id="app">
    <Tweet author='Alex' @myCustomEvent='handleChildEvent'/>
    <Tweet author='Not Alex' @myCustomEvent='handleChildEvent'/>
    <Tweet author='The Best Version of Alex' @myCustomEvent='handleChildEvent'/>
    <Footer :content="footerContent"/>
  </div>
</template>

<script>
import Tweet from "./components/Tweet.vue";
import Footer from "./components/Footer.vue";

export default {
  name: "App",
  components: {
    Tweet,
    Footer
  },
  data : function() {
    return {
      footerContent: "Footer"
    }
  },
  methods: {
    handleChildEvent: function(emitData) {
      this.footerContent = emitData;
    }
  }
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
