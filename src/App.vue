<template>
  <div id="app" class="container-fluid">
    <AddTodo/>
    <Todos/>
  </div>
</template>


<script>
import Todos from './components/Todos';
import AddTodo from './components/AddTodo';

export default {
  name: 'App',
  components: {
      Todos,
      AddTodo
  }
}
</script>

<style>
  #app {
    font-family: Avenir, Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    padding: 15px 25px;
  }

  body {
    background: #e8f7f0;
  }
</style>
