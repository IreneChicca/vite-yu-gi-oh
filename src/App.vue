<script>
import AppContent from "./components/AppContent.vue";
import BaseSelect from "./components/BaseSelect.vue";

export default {
  data() {
    return {
      title: "Yu-gi-oh API",
    };
  },

  components: { AppContent, BaseSelect },
};
</script>

<template>
  <h1 class="text-center border p-3 m-0">{{ title }}</h1>

  <div class="container p-4">
    <BaseSelect />
  </div>
  <AppContent></AppContent>
</template>

<style lang="scss">
@use "./styles/general.scss" as *;
</style>
