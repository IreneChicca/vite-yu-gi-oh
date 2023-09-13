<script>
export default {
  data() {
    return {};
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
        @change="$emit('selected-new-archetype')"
        class="form-select"
        aria-label="Default select example"
      >
        <option selected>Select ...</option>
        <option value="1" v-for="(type, i) in arch">{{ type }}</option>
      </select>
    </div>
  </div>
</template>
<style></style>
