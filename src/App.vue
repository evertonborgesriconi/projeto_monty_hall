<template>
  <h1>Poblema Monty Hall</h1>
  <Door :number="1" :hasGift="true" />
</template>

<script>
import Door from './components/Door.vue'
export default {
  name: "App",
  components: { Door },
};
</script>

<style>

* {
  box-sizing: border-box;
  font-family: "Montserrat", sans-serif;
}
body {
  color: #fff;
  background: linear-gradient(to left, #aa4b6b, #6b6b83, #3b8d99);
}
#app {
  display: flex;
  flex-direction: column;
  align-items: center;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
#app h1 {
  border: 1px solid black;
  background-color: #0004;
  padding: 20px;
  margin-bottom: 60px;
}
</style>
