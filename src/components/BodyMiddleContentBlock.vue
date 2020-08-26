<template>
  <v-container fluid class="middle">
    <v-row no-gutters>
      <v-col class="img-container">
        <v-img contain :src="content.imgUrl"></v-img>
      </v-col>
    </v-row>
    <v-row>
      <v-col class="title">
        {{ content.title }}
      </v-col>
    </v-row>
    <v-row>
      <v-col class="content">
        {{ content.content }}
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {
  name: 'BodyMiddleContentBlock',
  props: {
    content: Object,
  },
};
</script>

<style scoped>
.middle {
  padding: 0 17.9rem 0 0;
  width: 92.6rem;
}
.v-image {
  max-height: 23.6rem !important;
}
.img-container {
  text-align: center;
  margin-bottom: 10.3rem;
}
.title {
  text-align: left;
  font-size: 5.2rem !important;
  font-family: 'Avenir-Black' !important;
  margin-bottom: 2rem;
}
.content {
  text-align: left;
  font-size: 3.1rem;
  font-family: 'Avenir-Book';
  color: #3e5d5d;
  line-height: 6rem;
}
</style>
