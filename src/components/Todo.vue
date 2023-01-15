<template>
    <div class="item" v-bind:class="{ 'completed' : todo.completed }">
      <h2 @click="markComplete">{{ todo.title }}</h2>
      <i @click="onDelete(todo.id)" class="fa-regular fa-circle-xmark"></i>
    </div>
</template>

<script>
export default {
  name: 'Todo',
  props: [
    "todo"
  ],
  methods: {
    markComplete() {
      this.todo.completed = !this.todo.completed
    },
    onDelete(id) {
      this.$emit('delete-todo', id)
    },
  },
}
</script>

<style scoped>
.completed {
  text-decoration: line-through;
}

.item {
  display: flex;
  align-items: center;
  justify-content: space-between;
  width: 50vw;
}
</style>