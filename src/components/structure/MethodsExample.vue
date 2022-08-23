<template>
<div id="app-methods">
    <h1 v-text="'Message: ' + message" />
    <button @click="reverse" class="button">
        Invertir
    </button>
</div>
</template>

<script>
export default {
    el: "#app-methods",
    data: function () {
        return {
            message: "Hello word!",
        };
    },
    methods: {
        reverse: function() {
            this.message = this.message.split('').reverse().join('')
        }
    }
};
</script>

<style>
.button {
    background-color: #355575;
    border: none;
    color: white;
    padding: 8px 16px;
    text-align: center;
    text-decoration: none;
    display: inline-block;
    font-size: 16px;
    border-radius: 16px;
}

.button:hover {
    background-color: #6e89a4;
}
</style>
