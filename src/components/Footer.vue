<template>
  <v-footer app>
    <v-container fluid>
      <v-row>
        <FooterNavList
          v-for="(listItem, index) in listItems"
          :key="index"
          :title="listItem.title"
          v-bind:listItems="listItem.list">
        </FooterNavList>
      </v-row>
    </v-container>
    <v-img contain class="round-image" :src="imgRoundUrl" alt="round-1"></v-img>
  </v-footer>
</template>

<script>
import FooterNavList from './FooterNavList.vue';
import imgRound from '../assets/img/round-3.svg';

export default {
  name: 'Footer',
  components: {
    FooterNavList,
  },
  data() {
    return {
      imgRoundUrl: imgRound,
      listItems: [
        {
          title: 'SERVICES',
          list: ['Interior Design', 'Architecture', 'Furniture and Decor'],
        },
        {
          title: 'ABOUT',
          list: ['Philosophy', 'Our Strengths', 'Our Team'],
        },
        {
          title: 'PORTFOLIO',
          list: ['Residental', 'Commercial'],
        },
        {
          title: 'CONTACT US',
          list: [
            'Level 10, 4 Elizabeth St, Melbourne, Victoria 3000',
          ],
        },
      ],
    };
  },
};
</script>

<style scoped>
.v-footer {
  position: initial;
  background-color: #006665 !important;
  padding: 27.4rem 39.4rem 22.4rem 39.4rem;
  border-top-left-radius: 3rem !important;
}
.round-image {
  max-width: 81rem !important;
  position: absolute;
  left: 0;
  bottom: 0;
  z-index: 100;
}
</style>
