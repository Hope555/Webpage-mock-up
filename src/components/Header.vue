<template>
  <v-app-bar app flat color="#006665">
    <v-img class="logo" :src="imgUrl" alt="logo"></v-img>
    <div v-if="!isMobile" class="button-area">
      <v-btn text color="white">Services</v-btn>
      <v-btn text color="white">About</v-btn>
      <v-btn text color="white">Portfolio</v-btn>
      <v-btn text color="white">Contact Us</v-btn>
      <div class="sign-area">
        <v-btn class="signin-style" text color="white">Sign In</v-btn>
        <v-btn class="signup-style" color="#ceeef3">Sign Up</v-btn>
      </div>
    </div>
    <div v-else class="text-center menu-container">
      <v-menu offset-y>
        <template v-slot:activator="{ on, attrs }">
          <v-btn class="signup-style" color="#ceeef3" v-bind="attrs" v-on="on">Navigation</v-btn>
        </template>
        <v-list>
          <v-list-item>
            <v-list-item-title class="list-item-style">Services</v-list-item-title>
          </v-list-item>
          <v-list-item>
            <v-list-item-title class="list-item-style">About</v-list-item-title>
          </v-list-item>
          <v-list-item>
            <v-list-item-title class="list-item-style">Portfolio</v-list-item-title>
          </v-list-item>
          <v-list-item>
            <v-list-item-title class="list-item-style">Sign In</v-list-item-title>
          </v-list-item>
          <v-list-item>
            <v-list-item-title class="list-item-style">Sign Up</v-list-item-title>
          </v-list-item>
        </v-list>
      </v-menu>
    </div>
  </v-app-bar>
</template>

<script>
import logo from '../assets/img/logo-white.png';

export default {
  name: 'Header',
  data() {
    return {
      imgUrl: logo,
    };
  },
  computed: {
    isMobile() {
      if (this.$vuetify.breakpoint.name === 'xs'
          || this.$vuetify.breakpoint.name === 'sm'
          || this.$vuetify.breakpoint.name === 'md') {
        return true;
      }
      return false;
    },
  },
};
</script>

<style scoped>
.v-app-bar {
  padding: 12.7rem 39.4rem 0 39.4rem;
  height: 23.1rem !important;
  position: initial !important;
}
.logo {
  max-width: 29.2rem;
  top: -4.15rem !important;
  margin-right: 16.2rem;
}
.v-btn {
  text-transform: none;
  font-size: 3rem !important;
  min-height: 10.4rem !important;
  max-height: 10.4rem !important;
  padding: 0 7.5rem !important;
}
.sign-area {
  position: absolute;
  right: 0;
  top: 0;
}
.signup-style {
  color: #013838;
  border-radius: 5.2rem;
  min-width: 27.2rem !important;
  max-width: 27.2rem !important;
}
.menu-container {
  position: absolute;
  left: 50%;
  -ms-transform: translateX(-50%);
  transform: translateX(-50%);
}
.list-item-style {
  font-size: 3rem;
}
</style>
