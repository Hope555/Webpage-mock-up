<template>
  <v-app>
    <Header></Header>
    <Body></Body>
    <Footer></Footer>
  </v-app>
</template>

<script>
import Header from './components/Header.vue';
import Body from './components/Body.vue';
import Footer from './components/Footer.vue';

export default {
  name: 'App',
  components: {
    Header,
    Body,
    Footer,
  },
};
</script>

<style>
html {
  font-size: 0.3125vw !important; /* 10px */
  font-family: 'Avenir-Medium';
}
body {
  margin: 0;
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
</style>
