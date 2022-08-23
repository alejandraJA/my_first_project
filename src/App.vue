<template>
  <div id="app">
    <InputMessageConditionsVue />
    <LoopComponent />
    <MethodsExample />
  </div>
</template>

<script>
import LoopComponent from './components/structure/LoopComponent.vue';
import InputMessageConditionsVue from './components/structure/InputMessageConditions.vue';
import MethodsExample from './components/structure/MethodsExample.vue';

export default {
  name: 'App',
  components: {
    LoopComponent,
    InputMessageConditionsVue,
    MethodsExample
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
body {
  margin-bottom: 200px;
}
</style>
