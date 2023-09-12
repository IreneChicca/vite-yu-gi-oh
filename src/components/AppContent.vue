<script>
import axios from "axios";
import Card from "./Card.vue";

export default {
  data() {
    return {
      cards: [],
    };
  },

  methods: {
    fetchCards() {
      axios
        .get("https://db.ygoprodeck.com/api/v7/cardinfo.php?num=20&offset=0")
        .then((response) => {
          this.cards = response.data.data;
          console.log(this.cards);
        });
    },
  },

  components: { Card },

  created() {
    this.fetchCards();
  },
};
</script>
<template>
  <div class="content p-5">
    <div class="container d-flex flex-wrap justify-content-evenly p-3">
      <Card v-for="(card, i) in cards" :key="i" :card="card"></Card>
    </div>
  </div>
</template>
<style>
.content {
  background-color: #d48f38;
}
.container {
  background-color: #fff;
}
</style>
