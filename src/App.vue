<template>
  <div id="app">
    <ButtonCountVue message="Count"/>
    <ButtonCountWithMethodVue message="Second count"/>
  </div>
</template>

<script>
import ButtonCountVue from './components/ButtonCount.vue'
import ButtonCountWithMethodVue from './components/ButtonCountWithMethod.vue';

export default {
  name: 'App',
  components: {
    ButtonCountVue, 
    ButtonCountWithMethodVue,
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
