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
  <AppContent></AppContent>
</template>

<style lang="scss">
@use "./styles/general.scss" as *;
</style>
