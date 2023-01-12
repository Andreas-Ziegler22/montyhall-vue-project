<template>
  <div class="door-area">
    <div class="door-frame">
      <Gift v-if="open && hasGift" />
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

<style>
:root{
  --door-border: 5px solid brown:
}

.door-area{
  position: relative;
  width: 200px;
  height: 310px;
  border-bottom: 10px solid #aaa;
}
</style>
