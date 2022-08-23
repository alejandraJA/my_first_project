<template>

<!-- v-text es para evitar los cambios de pantalla (como el binding) -->
<!-- v-show para hacer invisible el elemento -->
<!-- v-if para desaparecer (gone) el elemento -->
<!-- v-else mostrar un valor en cado del if anterior-->

    <div id="app">
        <p v-text="'Este elemento se hace invisible: ' + message" v-show="message.length > 3"/>
        <p v-text="'Este elemento desaparece: ' + message" v-if="message.length > 3"/>
        <p v-text="'Escribe algo'" v-else/>
        <input class="input" type="text" v-model="message">
        <p class="nota" v-text="'Para poder ver estos cambios hay que abrir el inspector'"/>
    </div>
</template>

<script>
export default {
    el: '#app',
    data: function () {
        return {
            message: "Hello word!"
        };
    }
}
</script>

<style>
.input {
  background-color: #3a6c753b;
  border: none;
  color: white;
  padding: 8px 16px;
  text-decoration: none;
  display: inline-block;
  font-size: 16px;
  border-radius: 16px;
}
.nota {
    font-size: 12px;
    color: #46668f81;
}
</style>