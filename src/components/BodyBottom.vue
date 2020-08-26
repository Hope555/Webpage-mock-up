<template>
  <v-row no-gutters class="bottom">
    <v-col cols="12" md="6">
      <form v-bind:class="{ mobileStyle: isMobile }">
        <span class="title">Contact <span class="title-second">us</span></span><br>
        <input class="name-input-style" type="text" name="Name" placeholder="Name"><br>
        <input type="text" name="Email" placeholder="Email"><br>
        <textarea name="Message" placeholder="Message"></textarea><br>
        <v-btn color="#ff8473">Submit</v-btn>
      </form>
    </v-col>
    <v-col align-self="center" cols="12" md="6">
      <v-img class="display-image"
             v-bind:class="{ mobileStyle: isMobile }"
             :src="imgUrl"
             alt="melbourne"></v-img>
    </v-col>
    <v-img class="round-image" :src="imgRoundUrl" alt="round-2"></v-img>
  </v-row>
</template>

<script>
import img from '../assets/img/melbourne.png';
import imgRound from '../assets/img/round-2.svg';

export default {
  name: 'BodyBottom',
  data() {
    return {
      imgUrl: img,
      imgRoundUrl: imgRound,
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
.bottom {
  padding: 23.8rem 39.4rem 24.4rem 39.4rem;
  position: relative;
}
form {
  float: left;
  text-align: left;
  width: 96rem;
}
.title {
  font-family: 'Avenir-Black' !important;
  font-size: 9rem !important;
  color: black !important;
  margin-bottom: 9.1rem !important;
}
.title-second {
  font-family: 'Avenir-Book' !important;
}
input, textarea {
  border: 3px solid #e6ebeb;
  border-radius: 1.4rem;
  font-family: 'Avenir-Book';
  font-size: 3.5rem;
  line-height: 10.9rem;
  width: 96rem;
  padding-left: 3.8rem;
  margin-bottom: 5.2rem;
}
.name-input-style {
  margin-top: 9.1rem !important;
}
textarea {
  height: 32.7rem;
  margin-bottom: 8.2rem;
}
::placeholder {
  color: #809b9b;
  opacity: 1;
}
:-ms-input-placeholder {
  color: #809b9b;
}
::-ms-input-placeholder {
  color: #809b9b;
}
.v-btn {
  font-family: 'Avenir-Book';
  min-height: 14rem !important;
  max-height: 14rem !important;
  min-width: 48.1rem !important;
  max-width: 48.1rem !important;
  border-radius: 7rem;
  font-size: 3.6rem;
  text-transform: none;
  color: white;
}
.display-image {
  min-height: 79.2rem !important;
  max-height: 79.2rem !important;
  min-width: 106.2rem !important;
  max-width: 106.2rem !important;
  float: right;
  border-radius: 14.5rem 14.5rem 14.5rem 0rem;
}
.round-image {
  max-width: 23.9rem !important;
  position: absolute;
  right: 0;
  bottom: -18.3rem;
  z-index: 100;
}
.mobileStyle {
  float: none;
  margin-left: auto;
  margin-right: auto;
}
</style>
