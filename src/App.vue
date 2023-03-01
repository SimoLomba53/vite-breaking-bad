<script>

import MainPart from './components/MainPart.vue';
import axios from "axios";

export default {
  components: { MainPart },


  created() {
    axios.get("https://db.ygoprodeck.com/api/v7/cardinfo.php?num=10&offset=0").then((response) => {
      console.log(response);
    })
  },
};
</script>

<template>
  <MainPart />
</template>

<style scoped></style>
