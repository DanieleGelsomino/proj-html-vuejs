<template>
  <div class="">
    <div id="app">
      <Header />
      <Jumbotron />
      <Main />
      <Footer />
    </div>
  </div>
</template>

<script>
import Header from "@/components/Header.vue";
import Jumbotron from "@/components/Jumbotron.vue";
import Main from "@/components/Main.vue";
import Footer from "@/components/Footer.vue";
export default {
  name: "App",
  components: {
    Header,
    Main,
    Footer,
    Jumbotron,
  },
};
</script>

<style lang="scss">
@import "@/style/general";
Header {
  background-color: transparent;
}
</style>
