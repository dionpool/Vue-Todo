<script setup>
import todoItem from './components/todoItem.vue'
</script>

<template>
  <header>
    <h1>Todo list</h1>
  </header>

  <main>
    <div class="todo-wrapper">
      <form action="#">
        <input type="text" id="input-item" placeholder="Task...">
        <button class="addBtn" onclick="addTodo()">Add</button>
    </form>
    
    <ul id="todolist">
      <todoItem />
    </ul>
    </div>
  </main>
</template>