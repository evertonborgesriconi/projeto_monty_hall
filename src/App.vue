<template>
  <h1>Poblema Monty Hall</h1>
  <!-- <Door :number="1" :hasGift="true" /> -->
  <div class="form">
    <div v-if="!started">
      <label for="portsAmount">Quantas Portas</label>
      <input
        type="text"
        id="portsAmount"
        size="3"
        v-model.number="portsAmount"
      />
    </div>
    <div v-if="!started">
      <label for="selectedPort">Qual porta é a premiada</label>
      <input
        type="text"
        id="selectedPort"
        size="3"
        v-model.number="selectedPort"
      />
    </div>
    <button v-if="!started" @click="started = true">Iniciar</button>
    <button v-if="started" @click="started = false">Reiniciar</button>
  </div>
  <div class="doors" v-if="started">
    <div v-for="i in portsAmount" :key="i">
      <Door :number="i" :hasGift="i === selectedPort" />
    </div>
  </div>
</template>

<script>
import Door from "./components/Door.vue";
export default {
  name: "App",
  components: { Door },
  data() {
    return {
      started: false,
      portsAmount: 3,
      selectedPort: null,
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
.form {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  margin-bottom: 40px;
}
.form input {
  margin-left: 5px;
}
.form,
.form input,
.form button {
  margin-bottom: 10px;
  font-size: 1rem;
}
.doors {
  align-self: stretch;
  display: flex;
  flex-wrap: wrap;
}
</style>
