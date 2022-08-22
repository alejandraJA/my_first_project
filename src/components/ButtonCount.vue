<template>
  <div id="app">
    <h1>{{message}} {{count}}</h1>
  <button class = 'button' @click="count++">
    Count is: {{ count }}
  </button>
</div>
</template>

<script>
  export default {
    name: 'HelloWorld',
    props: {
      message: String
    }, 
    data() {
      return {
        count:0
      }
    },
  }
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  h3 {
    margin: 40px 0 0;
  }
  ul {
    list-style-type: none;
    padding: 0;
  }
  li {
    display: inline-block;
    margin: 0 10px;
  }
  a {
    color: #42b983;
  }
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
</style>
