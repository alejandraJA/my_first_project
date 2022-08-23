<template lang="en">
<div id="app">
    <h1>Lista de tareas</h1>
    <p v-for="(item, index) in task">
        <span v-text="item.message" />
        <small class="identificator" v-if="item.complete" v-text="' Completa'" />
        <small class="identificator" v-else v-text="' Incompleta'" />
    </p>
    <h2>Nueva tarea</h2>
    <input v-model="newTask" type="text" class="input" placeholder="Tarea">
    <button class="floatinButton" @click="addTask">+</button>
    <br>
    <small class="error" v-text="error" v-if="((newTask.length >= 1) && (newTask.length < 5))"></small>
    </input>
</div>
</template>

<script>
export default {
    el: '#app',
    data: function () {
        return {
            error: "Debe ser mayor de 5 carácteres",
            newTask: "",
            task: [{
                    message: 'Tarea 1',
                    complete: false
                },
                {
                    message: 'Tarea 2',
                    complete: true
                },
                {
                    message: 'Tarea 3',
                    complete: false
                },
                {
                    message: 'Tarea 4',
                    complete: true
                },
                {
                    message: 'Tarea 5',
                    complete: true
                },
                {
                    message: 'Tarea 6',
                    complete: false
                },
                {
                    message: 'Tarea 7',
                    complete: false
                },
                {
                    message: 'Tarea 8',
                    complete: false
                },
            ]
        }
    },
    methods: {
        addTask: function () {
            if (this.newTask.length > 5) {
                this.task.push({
                    message: this.newTask,
                    complete: false
                })
                this.newTask = ''
            } else {
                if(!this.newTask) {
                    this.error = 'El campo esta vacio'
                }
                else this.error = 'Debe ser mayor de 5 carácteres'
            }
        }
    }
}
</script>

<style>
.input {
    background-color: #355575;
    border: none;
    color: white;
    padding: 8px 16px;
    text-decoration: none;
    display: inline-block;
    font-size: 16px;
    border-radius: 16px 0px 0px 16px;
}

.input:focus {
    background-color: #6e89a4;
}

.input::placeholder {
    color: white
}

.floatinButton {
    background-color: #355575;
    border: none;
    color: white;
    padding: 8px 12px;
    font-weight: 900;
    text-align: center;
    text-decoration: none;
    display: inline-block;
    font-size: 16px;
    border-radius: 0px 16px 16px 0px;
}

.floatinButton:hover {
    background-color: #6e89a4;
}


.error {
    margin-top: 4px;
    color: rgb(197, 24, 24);
    font-size: 10px;
    align-items: flex-end;
}
</style>
