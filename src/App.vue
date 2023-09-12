<script>
import AppContent from "./components/AppContent.vue";

export default {
  data() {
    return {
      title: "ok",
    };
  },

  components: { AppContent },
};
</script>

<template>
  <h1>{{ title }}</h1>
</template>

<style lang="scss">
@use "./styles/general.scss" as *;
</style>
