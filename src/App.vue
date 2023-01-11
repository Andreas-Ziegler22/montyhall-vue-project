<template>
  <div id="app">
    <h1>Monty Hall problem</h1>
    <gift />
  </div>
</template>

<script>
import Gift from "./components/Gift.vue";

export default {
  components: { Gift },
  name: "App",
  comments: { Gift },
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
