<template>
  <div id="app">
    <!--InputMessageConditionsVue /-->
    <h1>Title</h1>
    <LoopComponent />
  </div>
</template>

<script>
import LoopComponent from './components/structure/LoopComponent.vue';
//import InputMessageConditionsVue from './components/structure/InputMessageConditions.vue';

export default {
  name: 'App',
  components: {
    LoopComponent,
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
