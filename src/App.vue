<template>
  <div id="app">
    <h1>Monty Hall problem</h1>
    <div class="form">
      <div v-if="!started">
        <label for="doorsAmount">How many doors?</label>
        <input
          type="text"
          id="doorsAmount"
          size="3"
          v-model.number="doorsAmount"
        />
      </div>
      <div v-if="!started">
        <label for="selectedDoor">What is the winning door?</label>
        <input
          type="text"
          id="doorsAmount"
          size="3"
          v-model.number="selectedDoor"
        />
      </div>
      <button v-if="!started" @click="started = true">Start</button>
      <button v-if="started" @click="started = false">Restart</button>
    </div>
    <div class="doors" v-if="started">
      <div v-for="i in doorsAmount" :key="i">
        <Door :hasGift="i === selectedDoor" :number="i" />
      </div>
    </div>
  </div>
</template>

<script>
import Door from "./components/Door.vue";

export default {
  name: "App",
  components: { Door },
  data: function () {
    return {
      started: false,
      doorsAmount: 3,
      selectedDoor: null,
    };
  },
};
</script>

<style>
* {
  box-sizing: border-box;
  font-family: "Montserrat", sans-serif;
}
body {
  color: #fff;
  background: linear-gradient(to right, #6a9113, #141517);
}
#app {
  display: flex;
  flex-direction: column;
  align-items: center;
}

#app h1 {
  border: 1px solid #000;
  background-color: #0004;
  padding: 20px;
  margin-bottom: 60px;
}
</style>
