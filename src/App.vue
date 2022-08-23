<template>
  <div id="app">
    <InputMessageConditionsVue />
  </div>
</template>

<script>
import InputMessageConditionsVue from './components/structure/InputMessageConditions.vue';

export default {
  name: 'App',
  components: {
    InputMessageConditionsVue
}
}
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
