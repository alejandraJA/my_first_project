<template>
    <div id="app">
        <h1>{{ message }} {{ count }}</h1>
        <button class='button' @click="increment">
            Count is: {{ count }}
        </button>
    </div>
</template>

<script>
export default {
    name: 'ButtonCountWithMethod',
    props: {
        message: String
    },
    data() {
        return {
            count: 0
        }
    },

    methods: {
        increment() {
            this.count++
            console.log(`Count with method is ${this.count}.`)
        }
    },

    mounted() {
        console.log(`The initial count is ${this.count}.`)
    }
}
</script>

<style>
.button {
    background-color: #355575;
    border: none;
    color: white;
    margin-top: 16px;
    padding: 8px 16px;
    text-align: center;
    text-decoration: none;
    display: inline-block;
    font-size: 16px;
    border-radius: 16px;
}
</style>