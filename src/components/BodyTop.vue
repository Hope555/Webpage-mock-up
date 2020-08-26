<template>
  <v-row no-gutters class="top">
    <v-col class="top-content" cols="12" md="6">
      <div class="top-content-container" v-bind:class="{ mobileStyle: isMobile }">
        <div class="title">Our Design</div>
        <div class="subtitle">Your Passion</div>
        <div class="content">
          Lorem ipsum dolor sit amet, consectetur adipiscing elit,
          sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.
          Quis ipsum suspendisse ultrices gravida.
          Risus commodo viverra maecenas accumsan lacus vel facilisis.
        </div>
        <v-btn color="#ff8473">Get A Free Consultation</v-btn>
      </div>
    </v-col>
    <v-col align-self="center" cols="12" md="6">
      <v-img class="display-image"
             v-bind:class="{ mobileStyle: isMobile }"
             :src="imgUrl"
             alt="interior"></v-img>
    </v-col>
    <v-img class="round-image" :src="imgRoundUrl" alt="round-1"></v-img>
  </v-row>
</template>

<script>
import img from '../assets/img/interior.jpg';
import imgRound from '../assets/img/round-1.svg';

export default {
  name: 'BodyTop',
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
.top {
  background-color: #006665;
  padding: 24.9rem 39.4rem 45.3rem 39.4rem;
  position: relative;
}
.top-content {
  text-align: left;
}
.top-content-container {
  width: 112.9rem;
}
.title {
  font-family: 'Avenir-Black' !important;
  font-size: 18.2rem !important;
  line-height: 18.2rem;
  color: white;
}
.subtitle {
  font-family: 'Avenir-Book';
  font-size: 18.2rem !important;
  line-height: 18.2rem;
  color: #adcece;
  padding-top: 3.2rem;
  padding-bottom: 13.7rem;
}
.content {
  font-family: 'Avenir-Book';
  font-size: 3.6rem !important;
  color: #adcece;
  padding-bottom: 13.7rem;
}
.v-btn {
  min-height: 14rem !important;
  max-height: 14rem !important;
  min-width: 58rem !important;
  max-width: 58rem !important;
  border-radius: 7rem;
  font-family: 'Avenir-Medium';
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
  border-radius: 14.5rem 14.5rem 0rem 14.5rem;
}
.mobileStyle {
  float: none;
  margin-left: auto;
  margin-right: auto;
}
.round-image {
  max-width: 39.1rem !important;
  position: absolute;
  right: 0;
  bottom: -88.3rem;
}
</style>
