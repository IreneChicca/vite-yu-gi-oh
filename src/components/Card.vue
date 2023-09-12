<script>
export default {
  data() {
    return {};
  },

  methods: {
    buildImgPath(imgName) {
      const imgUrl = new URL(imgName);
      return imgUrl.href;
      alert(imgUrl);
    },
  },

  props: { card: Object },
};
</script>
<template>
  <div class="ccard m-2 col-2">
    <img :src="buildImgPath(card.card_images[0].image_url)" alt="" />
    <h6 class="text-uppercase text-white p-3">{{ card.name }}</h6>
    <p>{{ card.type }}</p>
  </div>
</template>
<style>
.ccard {
  background-color: #d48f38;
  text-align: center;
}
</style>
