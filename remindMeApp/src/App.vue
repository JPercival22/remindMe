<template>
  <div id="app"> 
    <h1>remind<span class="blue-logo-text">Me</span></h1>
    <h2>{{ msg }}</h2>
    <h3>Essential Links</h3>
    <toDo-List></toDo-List>
  </div>
</template>

<script>
import toDoList from './components/toDoList.vue'

export default {
  name: 'app',
  components: {
    toDoList
  },
  data () {
    return {
      msg: 'The App that reminds you to do your to-do list'
    }
  }
}
</script>

<style lang="scss">
* {
  box-sizing: border-box;
}
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  background-color: #fff;
      display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    border: 1px solid black;
    border-radius: 3px;
    max-width: 600px;
    padding: 50px;
}

body {
    margin: 0 auto;
    max-width: 600px;
    background-color: #dfdedeef;
}
h1, h2 {
  color: black;
  font-weight: 700;
    .blue-logo-text{
      color: dodgerblue;
    }
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
</style>
