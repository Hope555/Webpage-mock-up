<template>
  <v-main>
    <v-container fluid>
      <BodyTop></BodyTop>
      <BodyMiddle></BodyMiddle>
      <BodyBottom></BodyBottom>
    </v-container>
  </v-main>
</template>

<script>
import BodyTop from './BodyTop.vue';
import BodyMiddle from './BodyMiddle.vue';
import BodyBottom from './BodyBottom.vue';

export default {
  name: 'Body',
  components: {
    BodyTop,
    BodyMiddle,
    BodyBottom,
  },
};
</script>

<style scoped>
.v-main, .container {
  padding: 0 !important;
}
</style>
