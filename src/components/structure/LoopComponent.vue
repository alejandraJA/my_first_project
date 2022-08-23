<template lang="en">
<div id="app-example-loop">
    <h1>Lista de tareas</h1>
     <ul>
          <p v-for="(item, index) in items">
          <span v-text="item.mensaje"/>
          <small class="identificator" v-if="item.complete" v-text="' Completa'"/>
          <small class="identificator" v-else v-text="' Incompleta'" />
          </p>
    </ul>
</div>
</template>
<script>
export default {
    el: '#app-example-loop',
    data() {
        return {
            items: [
                { mensaje: 'Tarea 1', complete: false },
                { mensaje: 'Tarea 2', complete: true },
                { mensaje: 'Tarea 3', complete: false },
                { mensaje: 'Tarea 4', complete: true },
                { mensaje: 'Tarea 5', complete: true },
                { mensaje: 'Tarea 6', complete: false },
                { mensaje: 'Tarea 7', complete: false },
                { mensaje: 'Tarea 8', complete: false },
                { h: 'Tarea 9', f: true },
            ]
        }
    },
}
</script>
<style lang="">
</style>