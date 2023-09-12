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
  <div class="ccard m-3 col-2">
    <img :src="buildImgPath(card.card_images[0].image_url)" alt="" />
    <p>{{ card.name }}</p>
    <p>{{ card.type }}</p>
  </div>
</template>
<style></style>
