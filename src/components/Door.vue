<template>
  <div class="door-area">
    <div class="door-frame">
      <Gift />
    </div>
    <div class="door">
      <div class="number">{{ number }}</div>
      <div class="knobDoor"></div>
    </div>
  </div>
</template>

<script>
import Gift from "./Gift.vue";

export default {
  name: "Door-component",
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
