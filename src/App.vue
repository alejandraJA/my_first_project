<template>
<div id="app">
    <!--InputMessageConditionsVue />
    <LoopComponent />
    <MethodsExample /-->
    <ProjectIntegrate />
</div>
</template>

<script>
import ProjectIntegrate from './components/structure/ProjectIntegrate.vue';
//import LoopComponent from './components/structure/LoopComponent.vue';
//import InputMessageConditionsVue from './components/structure/InputMessageConditions.vue';
//import MethodsExample from './components/structure/MethodsExample.vue';

export default {
    name: 'App',
    components: {
        ProjectIntegrate
    }
}
</script>

<style>
#app {
    font-family: Avenir, Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    color: #2c3e50;
    margin-left: 2%;
    margin-right: 2%;
    margin-top: 2%;
    margin-bottom: 2%;
}

body {
    margin-bottom: 200px;
}
</style>
