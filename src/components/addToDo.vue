<template>
    <div>
      <form @submit="addTodo">
        <input type="text" v-model="title" name="title">
        <button type="submit">Add</button>
      </form>
    </div>
  </template>

<script>
  import { v4 as uuidv4 } from 'uuid'
  export default {
    name: 'AddTodo',
    data() {
      return {
        title: ''
      }
    },
    methods: {
      addTodo(e) {
        e.preventDefault();
        const newTodoObj = {
          id: uuidv4(),
          title: this.title,
          completed: false
        }
        this.$emit('add-todo', newTodoObj);
        this.title = '';
      }
    }
  }
</script>

<style scoped>
form {
  display: flex;
  gap: .3rem;
  width: 100%;
}

form input {
  width: 100%;
  border-radius: 5px;
  padding: .5rem;
  border: none;
  background-color: #d2d1d8;
}

button {
  border-radius: 5px;
  background-color: #472bff;
  color: white;
  border: none;
  padding: 0 1em;
}

</style>