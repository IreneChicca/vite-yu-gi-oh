<script>
import axios from "axios";
import Card from "./Card.vue";
import BaseSelect from "./BaseSelect.vue";

export default {
  data() {
    return {
      cards: [],
      archetypes: [],
    };
  },

  methods: {
    fetchCards() {
      axios
        .get("https://db.ygoprodeck.com/api/v7/cardinfo.php?num=20&offset=0")
        .then((response) => {
          this.cards = response.data.data;
        });
    },

    // creo metodo che richiama da API gli archetipi
    fetchArchetype() {
      axios
        .get("https://db.ygoprodeck.com/api/v7/archetypes.php")
        .then((risp) => {
          const arrayLength = risp.data.length;

          for (let i = 1; i < arrayLength; i++) {
            this.archetypes.push(risp.data[i].archetype_name);
          }
        });
    },
  },

  components: { Card, BaseSelect },

  created() {
    this.fetchCards();
    this.fetchArchetype();
  },
};
</script>
<template>
  <div class="container p-4">
    <BaseSelect :arch="this.archetypes" class="w-25" />
  </div>

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
