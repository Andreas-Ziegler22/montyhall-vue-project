<template></template>

<script>
import Gift from "./Gift.vue";

export default {
  name: "Door-componet",
  comments: { Gift },
  props: {
    number: {},
    hasGift: { type: Boolean },
  },
  data: function () {
    return {
      open: false,
      selected: false,
    };
  },
};
</script>

<style></style>
