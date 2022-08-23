<template>
    <div id="app">
        <h1>Message: {{ message }}</h1>
        <input class="input" type="text" v-model="message">
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
</style>