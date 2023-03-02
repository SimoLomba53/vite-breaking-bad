<script>
import HeaderPart from './components/HeaderPart.vue';
import MainPart from './components/MainPart.vue';
import BaseSearch from './components/BaseSearch.vue'
import bootstrap from "../package-lock.json";
import axios from "axios";

export default {
  data() {
    return {
      cards: [],
    };
  },

  components: { HeaderPart, MainPart },


  created() {
    axios.get("https://db.ygoprodeck.com/api/v7/cardinfo.php?num=10&offset=0").then((response) => {
      this.cards = response.data.data;
    })
  },
};
</script>

<template>
  <HeaderPart />
  <MainPart :cards="cards" />
</template>

<style scoped></style>
