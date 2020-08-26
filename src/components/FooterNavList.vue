<template>
  <v-col cols="12" md="3">
    <span>{{ title }}</span>
    <ul>
      <li
        v-for="(listItem, index) in listItems"
        :key="index"
      >
        <v-btn v-if="!isContact" text color="#c7dddd">{{ listItem }}</v-btn>
        <div class="address" v-else>{{ listItem }}</div>
        <v-btn class="email-button" v-if="isContact" color="#027978" depressed>
          interior_studio@gmail.com
          <i class="iconfont icon-send"></i>
        </v-btn>
      </li>
    </ul>
  </v-col>
</template>

<script>
export default {
  name: 'FooterNavList',
  props: {
    title: String,
    listItems: Array,
  },
  data() {
    return {
      isContact: this.title === 'CONTACT US',
    };
  },
};
</script>

<style scoped>
.col {
  text-align: left;
  padding: 0;
}
span {
  color: white;
  font-family: 'Avenir-Medium';
  font-size: 3.6rem;
}
.v-btn, .address {
  font-family: 'Avenir-Book';
  font-size: 3.6rem;
  text-transform: none;
  padding: 0 !important;
  margin-top: 6rem;
}
.address {
  width: 64rem;
  text-align: left;
  margin-left: auto;
  margin-right: auto;
}
.email-button {
  height: 10.2rem !important;
  width: 64rem;
  color: white;
  font-family: 'Avenir-Book';
  border-radius: 1.3rem;
}
i {
  margin-left: 3.8rem;
}
ul {
  list-style-type: none;
  color: #c7dddd;
  margin: 0;
  padding: 0;
}
</style>
