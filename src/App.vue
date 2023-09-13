<script>
import AppContent from "./components/AppContent.vue";

export default {
  data() {
    return {
      title: "Yu-gi-oh API",
    };
  },

  components: { AppContent },
  methods: {
    selectArchetype() {
      console.log("ok");
    },
  },
};
</script>

<template>
  <h1 class="text-center border p-3 m-0">{{ title }}</h1>

  <div class="container p-4">
    <!-- <BaseSelect @selected-new-archetype="selectArchetype" /> -->
  </div>
  <AppContent></AppContent>
</template>

<style lang="scss">
@use "./styles/general.scss" as *;
</style>
