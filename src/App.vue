<template>
  <div id="app">
    <Todos v-bind:todos="todos"/>
    <AddTodo v-on:add-todo="addTodo"/>
  </div>
</template>

<script>
import Todos from './components/todos.vue';
import AddTodo from './components/addToDo.vue';
export default {
  name: 'app',
  components: {
    Todos,
    AddTodo
  },
  data() {
    return {
      todos: [
        {
          id: 1,
          title: 'Go workout',
          completed: false
        },
        {
          id: 2,
          title: 'Do laundry',
          completed: false
        },
        {
          id: 3,
          title: 'Cook food',
          completed: false
        },
        {
          id: 4,
          title: 'Clean up room',
          completed: false
        },
        {
          id: 5,
          title: 'Finish work',
          completed: false
        }
      ],
    }
  },
  methods: {
    addTodo(newTodoObj) {
      this.todos = [...this.todos, newTodoObj];
    }
  }
}
</script>
<style>
</style>


<!-- <script setup>
import todos from './components/todos.vue'
import addToDo from './components/addToDo.vue'
</script>

<template>
  <header>
    <h1>Todo list</h1>
  </header>

  <main>
    <div class="todo-wrapper">
      <addToDo @add-todo-event="addToDoItem" />
    
    <ul id="todolist">
      <todos v-bind:todoEntries="todoEntries"/>
    </ul>
    </div>
  </main>
</template> -->