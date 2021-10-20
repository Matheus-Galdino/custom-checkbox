<template>
  <h1>Checkbox customizada</h1>
  <Checkbox v-model="checked" id="checkbox" label="Manter-se conectado"/>
</template>

<script>
import Checkbox from "./components/Checkbox.vue";

export default {
  name: "App",
  components: {
    Checkbox,
  },
  data() {
    return {
      checked: true,
    };
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
