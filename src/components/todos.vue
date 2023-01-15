<template>
    <div>
        <ul>
            <li v-bind:key="todo.id" v-for="todo in todos">
                <Todo @delete-todo="$emit('delete-todo', todo.id)" v-bind:todo="todo" />
            </li>
        </ul>
    </div>
</template>

  <script>
    import Todo from './todo.vue';
    export default {
        name: 'Todos',
        components: {
            Todo
        },
        props: [
        "todos"
        ],
        emits: ['delete-todo'],
  }
  </script>

  <style scoped>
  ul {
    list-style: none;
    align-items: center;
  }
  </style>