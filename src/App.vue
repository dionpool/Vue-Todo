<script setup>
import todos from './components/todos.vue'
import todoItem from './components/todoItem.vue'
</script>

<template>
  <header>
    <h1>Todo list</h1>
  </header>

  <main>
    <div class="todo-wrapper">
     <form @submit="addToDo">
      <input type="text" v-model="title" name="title" placeholder="Task...">
      <button type="submit">Add</button>
    </form>
    
    <ul id="todolist">
      <todos />
    </ul>
    </div>
  </main>
</template>