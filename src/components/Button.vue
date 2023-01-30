<template></template>

<script lang="ts">
export default {
  name: "Butt",
  props: {
    text: {
      type: String,
      required: true,
    },
    title: {
      type: String,
      required: true,
    },
    content: {
      type: String,
    },
    type: {
      type: String,
      default: "primary",
    },
  },
};
</script>

<style scoped></style>
