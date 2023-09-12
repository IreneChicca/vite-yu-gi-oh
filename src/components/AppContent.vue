<script>
import axios from "axios";
import Card from "./Card.vue";

export default {
  data() {
    return {
      cards: [],
    };
  },

  components: { Card },

  created() {
    axios
      .get("https://db.ygoprodeck.com/api/v7/cardinfo.php?num=20&offset=0")
      .then((response) => {
        this.cards = response.data.data;
        console.log(this.cards);
      });
  },
};
</script>
<template></template>
<style></style>
