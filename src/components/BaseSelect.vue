<script>
export default {
  data() {
    return {
      selectedType: "",
    };
  },
  emits: ["selected-new-archetype"],

  props: { arch: Array },

  methods: {},
};
</script>
<template>
  <div>
    <div class="form-group">
      <label for="exampleFormControlSelect1" class="mb-3"
        >Seleziona Archetipo</label
      >
      <select
        @change="$emit('selected-new-archetype', selectedType)"
        class="form-select"
        aria-label="Default select example"
        v-model="selectedType"
      >
        <option selected value="">Select ...</option>
        <option :value="type" v-for="(type, i) in arch">{{ type }}</option>
      </select>
    </div>
  </div>
</template>
<style></style>
