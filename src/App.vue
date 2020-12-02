<template>
  <div>
    <h1>Hello Ankit Srivastava</h1>
    <TodoList />
  </div>
</template>

<script>
import TodoList from "./components/TodoList"

export default {
  name: "App",
  components: {
    TodoList
  }
}
</script>

<style>

body{
  background-color: #761980;
}
</style>