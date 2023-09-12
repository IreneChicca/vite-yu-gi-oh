<script>
import AppContent from "./components/AppContent.vue";

export default {
  data() {
    return {
      title: "Yu-gi-oh API",
    };
  },

  components: { AppContent },
};
</script>

<template>
  <h1 class="text-center border p-3 m-0">{{ title }}</h1>
  <AppContent></AppContent>
</template>

<style lang="scss">
@use "./styles/general.scss" as *;
</style>
