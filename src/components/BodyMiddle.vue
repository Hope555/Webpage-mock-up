<template>
  <v-container fluid class="middle">
    <v-row no-gutters>
      <v-col class="title">
        Interior design
        <br>
        <span class="subtitle">is for everyone.</span>
      </v-col>
    </v-row>
    <v-row class="content">
      <v-col class="content-title" cols="12" md="2">
        <span class="content-title-text">Good for your</span>
      </v-col>
      <v-col class="content-main-content" cols="12" md="5">
        <BodyMiddleContentBlock v-bind:content="contents[0]"></BodyMiddleContentBlock>
      </v-col>
      <v-col class="content-main-content" cols="12" md="5">
        <BodyMiddleContentBlock v-bind:content="contents[1]"></BodyMiddleContentBlock>
      </v-col>
    </v-row>
    <v-row class="content">
      <v-col class="content-title" cols="12" md="2">
        <span class="content-title-text">Good for You</span>
      </v-col>
      <v-col class="content-main-content" cols="12" md="5">
        <BodyMiddleContentBlock v-bind:content="contents[2]"></BodyMiddleContentBlock>
      </v-col>
      <v-col class="content-main-content" cols="12" md="5">
        <BodyMiddleContentBlock v-bind:content="contents[3]"></BodyMiddleContentBlock>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
import icon1 from '../assets/img/icon-1.svg';
import icon2 from '../assets/img/icon-2.svg';
import icon3 from '../assets/img/icon-3.svg';
import icon4 from '../assets/img/icon-4.svg';
import BodyMiddleContentBlock from './BodyMiddleContentBlock.vue';

export default {
  name: 'BodyMiddle',
  components: {
    BodyMiddleContentBlock,
  },
  data() {
    return {
      contents: [
        {
          imgUrl: icon1,
          title: 'Find your happy place',
          content: `Lorem ipsum dolor sit amet, consectetur adipiscing elit,
                    sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.
                    Quis ipsum suspendisse ultrices gravida.
                    Risus commodo viverra maecenas accumsan lacus vel facilisis.`,
        },
        {
          imgUrl: icon2,
          title: 'Delightfully affordable',
          content: `Lorem ipsum dolor sit amet, consectetur adipiscing elit,
                    sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.
                    Quis ipsum suspendisse ultrices gravida.
                    Risus commodo viverra maecenas accumsan lacus vel facilisis.`,
        },
        {
          imgUrl: icon3,
          title: 'Create a lasting relationship',
          content: `Lorem ipsum dolor sit amet, consectetur adipiscing elit,
                    sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.
                    Quis ipsum suspendisse ultrices gravida.
                    Risus commodo viverra maecenas accumsan lacus vel facilisis.`,
        },
        {
          imgUrl: icon4,
          title: 'We work with 200 vendors',
          content: `Lorem ipsum dolor sit amet, consectetur adipiscing elit,
                    sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.
                    Quis ipsum suspendisse ultrices gravida.
                    Risus commodo viverra maecenas accumsan lacus vel facilisis.`,
        },
      ],
    };
  },
};
</script>

<style scoped>
.middle {
  background-color: #f7fbfb;
  border-bottom-right-radius: 10rem;
}
.title {
  padding: 16.7rem 39.4rem;
  color: black;
  font-family: 'Avenir-Black' !important;
  font-size: 9rem !important;
  line-height: 11rem;
  text-align: left;
}
.subtitle {
  font-family: 'Avenir-Book';
}
.content {
  padding: 16.7rem 39.4rem;
}
.content-title {
  font-size: 3.7rem;
  font-family: 'Avenir-BlackOblique';
  padding: 0;
  width: 35.4rem;
  text-align: left;
}
.content-title-text {
  display: inline-block;
  margin-top: 8rem;
}
.content-title-text::before {
  display: inline-block;
  content: "";
  border-top: .6rem solid black;
  width: 6.8rem;
  margin-right:1.7rem;
  transform: translateY(-1rem);
}
.content-main-content {
  padding: 0;
}
</style>
