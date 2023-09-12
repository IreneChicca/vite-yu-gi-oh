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

    buildImgPath(imgName) {
      const imgUrl = new URL(imgName);
      return imgUrl.href;
      alert(imgUrl);
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
    <div class="container">
      <div v-for="card in cards">
        <p>{{ card.name }}</p>
        <p>{{ card.type }}</p>

        <img :src="buildImgPath(card.card_images[0].image_url)" alt="" />
      </div>
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
