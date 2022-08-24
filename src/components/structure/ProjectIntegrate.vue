<template lang="en">
<div id="app">
    <section>
        <h1>Lista de tareas</h1>
        <p v-if="completeTask" v-text="'Tareas completadas ' + completeTask" />
        <p v-if="inCompleteTask"v-text="'Tareas incompletas ' + inCompleteTask" />
        <p class="card" v-for="(item, index) in tasks">
            <span v-text="item.message" />
            <input class="checkbox" @click="item.complete = false" type="checkbox" checked v-if="item.complete" />
            <input class="checkbox" @click="item.complete = true" type="checkbox" v-else />
        </p>
        <br>
        <p>Nueva tarea</p>
        <input v-model="newTask" type="text" class="input" placeholder="Tarea">
        <button class="floatinButton" @click="addTask">+</button>
        <br>
        <small class="error" v-text="error" v-if="((newTask.length >= 1) && (newTask.length < 5))"></small>
        </input>
    </section>
    <section>
        <pre>
        {{$data}}
        </pre>
    </section>
</div>
</template>

<script>
export default {
    data: function () {
        return {
            error: "Debe ser mayor de 5 carácteres",
            newTask: "",
            tasks: [{
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
            ]
        }
    },
    methods: {
        addTask: function () {
            if (this.newTask.length > 5) {
                this.tasks.push({
                    message: this.newTask,
                    complete: false
                })
                this.newTask = ''
            } else {
                if (!this.newTask) this.error = 'El campo esta vacio'
                else this.error = 'Debe ser mayor de 5 carácteres'
            }
        }
    },
    computed: {
        completeTask: function () {
            return this.tasks.filter(function (task) {
                return task.complete
            }).length
        },
        inCompleteTask: function () {
            return this.tasks.filter(function (task) {
                return !task.complete
            }).length
        }
    },
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

.checkbox {
    cursor: pointer;
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
    cursor: pointer;
}

.card {
    background-color: #355575;
    border-radius: 16px;
    padding-top: 8px;
    margin-top: 4px;
    margin-bottom: 4px;
    padding-bottom: 8px;
    padding-left: 16px;
    padding-right: 16px;
}

.error {
    margin-top: 4px;
    color: #c51818;
    font-size: 10px;
    align-items: flex-end;
}

#app {
    display: flex;
    flex-direction: row;
    flex-wrap: wrap;
}

#app>section {
    width: 48%;
    padding: 1%;
}

#app>section>pre {
    background-color: #0b0c0ca1;
    border-radius: 16px;
    padding-top: 16px;
    padding-left: 16px;
    padding-bottom: 16px;
    padding-right: 16px;
}
</style>
