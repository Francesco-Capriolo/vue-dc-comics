<template>
  <div id="app">
    <Header />
    <IconDC />
    <Container />
    <Footer />
  </div>
</template>

<script>
import Header from "./components/Header.vue";
import IconDC from "./components/IconDC.vue";
import Container from "./components/Container.vue";
import Footer from "./components/Footer.vue";

export default {
  name: "App",
  components: {
    Header,
    IconDC,
    Container,
    Footer,
  },
};
</script>

<style>
@import "./assets/scss/style.scss";

#app {
  font-size: 12px;
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}
</style>
