<script>
export default {
  data() {
    return {};
  },
  emits: ["selected-new-archetype"],

  methods: {},
};
</script>
<template>
  <div>
    <form>
      <div class="form-group">
        <label for="exampleFormControlSelect1" class="mb-3"
          >Seleziona Archetipo</label
        >
        <select
          @change="$emit('selected-new-archetype')"
          class="form-select"
          aria-label="Default select example"
        >
          <option selected>Open this select menu</option>
          <option value="1">One</option>
          <option value="2">Two</option>
          <option value="3">Three</option>
        </select>
      </div>
    </form>
  </div>
</template>
<style></style>
