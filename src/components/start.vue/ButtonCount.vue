<template>
  <div id="app">
    <h1>{{ message }} {{ count }}</h1>
    <button class='button' @click="count++">
      Count is: {{ count }}
    </button>
  </div>
</template>

<script>
export default {
  name: 'ButtonCount',
  props: {
    message: String
  },
  data() {
    return {
      count: 0
    }
  },
}
</script>

<style scoped>
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
