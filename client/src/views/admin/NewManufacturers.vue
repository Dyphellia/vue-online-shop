<template>
  <manufacturer-form @save-manufacturer="addManufacturer" :model="model">
  </manufacturer-form>
</template>

<script>
import ManufacturerForm from "@/components/ManufacturerForm";
export default {
  components: {
    ManufacturerForm
  },
  computed: {
    model() {
      return {};
    }
  },
  methods: {
    addManufacturer(model) {
      this.$store.dispatch("addManufacturer", {
        manufacturer: model
      });
    }
  }
};
</script>

<style lang="scss" scoped></style>
